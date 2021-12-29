# sf__legacy_vagrant
task_B6.5.2

Abay Zhumageldinov
DevOps-17

Vagrantfile запускает Linux машину на VirtualBox и устанавливает DB PostgreSQL.

VM - hashicorp/bionic64
DB - PostgreSQL:8.4.22

Проверка:

vagrant ssh

su - postgres

/usr/local/pgsql/bin/initdb -D /usr/local/pgsql/data
/usr/local/pgsql/bin/postgres -D /usr/local/pgsql/data >logfile 2>&1 &
/usr/local/pgsql/bin/createdb test
/usr/local/pgsql/bin/psql test
