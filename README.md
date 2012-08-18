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


y mas...
