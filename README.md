# xUI, temaplates simples pero poderosos #

como usar:

    var data = { user: { name: 'Pepe', age: null } };

    xUI.template("Mi nombre es ${ user.name }, y tengo ${ user.age|default:'varios' } años.")
    xUI.render(data)

    // Mi nombre es Pepe, y tengo varios años.


y también viene con filtros :)

default:
upper
lower
title
