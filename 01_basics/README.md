# Basis-Setup

```ansible```, ```ansible-playbook```
und die anderen Programme benötigen eine ```ansible.cfg```-Datei.

mit aufsteigendem Vorrang:
1. /etc/ansible/ansible.cfg
2. ./ansible.cfg
3. $ANSIBLE_CONFIG

## Wichtig:
* Inventory
* Become-User

## Windows als Control Node

... wird nicht standardmäßig supported, kann aber mit Hilfe des Linux-Subsystems zurechtgefrickelt werden:
https://geekmonkey.de/ansible-unter-windows/

## Sonstiges
* Fast alles kann über die Kommandozeile umgestellt werden.
* In AWX werden diese Settings über die Job-Templates vorgenommen.
* Ein static-Inventory würde ich im yaml-Format aufbauend auf dem Beispiel aufbauen.

Auf jedem ```control node``` solltet ihr für lokale Änderungen folgende Zeile in 
eure .vimrc einfügen, damit wird der vim zumindest benutzbar für yaml:

```.shell
autocmd FileType yaml setlocal ai ts=2 sw=2 et
```

## Werkzeuge

Empfehlenswert ist ```Idea``` (vielleicht Overkill)
sowie ```Visual Studio Code```, natürlich in der freien Fassung ```VSCodium``` ohne 
Telemetrie: https://github.com/VSCodium/vscodium/releases

Zum Prüfen ```yamllint``` sowie ```ansible-lint```

# Aufgaben

* Passt euer Inventory an euren Host (IP-Adresse) an.
* Prüft die Einstellungen mit ```ansible-inventory --list```

# Ad-Hoc Kommandos

```ansible -m setup localhost```

# Dokumentation mit ```ansible-doc```

Listet neben Modulen auch andere plugins wie ```lookup``` auf.
