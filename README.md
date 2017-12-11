# Happy Servers

An Ansible configuration for configuring Happy Prime servers.

## Initial server setup

* Configure the "[first 5 minutes on a server](https://plusbryan.com/my-first-5-minutes-on-a-server-or-essential-security-for-linux-servers)" with `ansible-playbook all-initial-setup.yml -i {{ host }}`


* `pip install passlib`
* `python -c "from passlib.hash import sha512_crypt; import getpass; print(sha512_crypt.encrypt(getpass.getpass()))"`
* Add password to `temp_user_password` in `vars.yml`
* `ansible-playbook all-initial-setup.yml --limit={{ hostname }}`


Inspiration from:
*
* https://github.com/chhantyal/5minutes

http://docs.ansible.com/ansible/latest/faq.html#how-do-i-generate-crypted-passwords-for-the-user-module
--ask-become-pass
