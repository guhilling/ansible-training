# Variablen

... sind leider grundsätzlich global, es gibt aber einen kleinen Trick.

## Aufruf von Roles

Hier gibt es verschiedene Möglichkeiten:
1. ```import_roles``` in Task
2. ```include_roles``` in Task
3. ```roles``` auf Play-Ebene.

## Variablenvorrang

https://docs.ansible.com/ansible/latest/user_guide/playbooks_variables.html#variable-precedence-where-should-i-put-a-variable

Oder kurz:
* Die meisten Regeln folgen dem Prinzip: Speziell vor Allgemein
* ```-e``` und ```-u``` sind klare Ausnahmen...
* role defaults sind klare Überraschungen (siehe Beispiele)
* Wichtig: https://docs.ansible.com/ansible/latest/user_guide/playbooks_reuse_roles.html
