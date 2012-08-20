# xUI, temaplates simples en javascript pero poderosos #

como usar:

    var data = { user: { name: 'Pepe', age: null } };

    xUI.template("Mi nombre es ${ user.name }, y tengo ${ user.age|default:'varios' } años.")
    xUI.render(data)

    // Mi nombre es Pepe, y tengo varios años.


## y también viene con filtros :) ##

**default**, asigna un valor por defecto

    ${ user.age|default:'varios' }
    // varios


**upper**, transforma a MAYUSCULAS

    ${ user|upper }
    // PEPE


**lower**, transforma a minusculas

    ${ user|lower }
    // pepe


**title**, hace un título con el string de la variable.
    
    ${ lorem|title }
    // Lorem Ipsum Dolor Sit Amet


**toLocalDate**, pasa una fecha al formato local

    ${ data.pub_date|toLocalDate }
    // Sábado, 18 de Agosto, 2012


**getDateDayName**, devuelve el nombre del día
    
    ${ data.pub_date|getDateDayName }
    // Sábado


**getDateDay**, devuelve el número del día en el mes en dos dígitos, 0x para los menores a 10

    ${ data.pub_date|getDateDay }
    // 18


**getDateMonthName**, devuelve el nombre del mes

    ${ data.pub_date|getDateMonthName }
    // Agosto


**getDateMonth**, devuelve el número de mes

    ${ data.pub_date|getDateMonth }
    // 8


**getDateYear**, devuelve el año
    
    ${ data.pub_date|getDateYear }
    // 2012


**getTimeHours**, devuelve la hora en formato 24hs

    ${ data.pub_date|getTimeHours }
    // 16


**getTimeMinutes**, devuelve los minutos en dos dígitos, 0x para los menores a 10

    ${ data.pub_date|getTimeMinutes }
    // 20


**getTimeSeconds**, devuelve los segundos en dos dígitos, 0x para los menores a 10

    ${ data.pub_date|getTimeSeconds }
    // 32


**length**, cuenta los items de un objeto

    var data = [1, 2, 3, 'a', 'b'];
    ...

    ${ data|length }
    // 5
    

**truncateWords**, corta una porción de un string en __n__ palabras
    
    var data = "Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor";
    ...

    ${ data|truncateWords:6 }
    // "Lorem ipsum dolor sit amet, consectetur"
