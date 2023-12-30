# Modularisierung (Kapitel 5, 6)

https://docs.ansible.com/ansible/latest/user_guide/playbooks_reuse.html#playbooks-reuse

## Möglichkeiten

Grundsätzlich sind die _include_-Varianten dynamisch, die _import_-Varianten dagegeben statisch.
Dies hat z.B. Auswirkungen bei der Verwendung von ```--list-tags``` und ```--list-tasks```: Dynamsich
eingebundene Dateien werden nicht mit einbezogen!

* Tasks:
    * ```import_tasks```
    * ```include_tasks```
* Playbooks:
    * ```import_playbook```
* Roles:
    * ```include_role```
    * ```import_role```
    * ```roles```-Keyword auf Play-Ebene

Faustregel: Wenn möglich, die statische Variante verwenden und _Roles_ verwenden! (https://docs.ansible.com/ansible/latest/user_guide/playbooks_reuse_roles.html)

Bearbeiten: Kapitel 4/Yaml!