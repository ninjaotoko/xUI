# xUI, temaplates simples pero poderosos #

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

**getDateDayName**, devuelve el nombre del día

**getDateDay**, devuelve el número del día en el mes

**getDateMonthName**, devuelve el nombre del mes

**getDateMonth**, devuelve el número de mes

**getDateYear**, devuelve el año

**getTimeHours**, devuelve la hora
**getTimeMinutes**, devuelve los minutos
**getTimeSeconds**, devuelve los segundos
