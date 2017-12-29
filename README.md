# Vagrant box for PHP Development

## Installation

1. Make sure you have `vagrant`/`Virtualbox`/`Ansible` installed
2. Clone this repo (and optionally delete .git directory)

```bash
> git clone --depth=1 https://github.com/nev3rm0re/vagrant-dev-php-box my-dev-php-box
> git rm my-dev-php-box/.git
``` 
3. Check and/or update variables in `provision/playbook.yml`
4. Run `vagrant up`

   This will download Virtualbox box and Ansible roles from Ansible Galaxy
   and provision your new machine according to your variables.

5. Go to http://192.168.50.150 (default IP, set in Vagrantfile) and you should see `phpinfo()` output

## History

I caught myself re-creating my Vagrantfile everytime I start to work on a
new PHP project. Thanks to wonderful Ansible roles created by [@geerlingguy](https://github.com/geerlingguy),
it is super easy, but still requires some work. To save time for myself and
my colleagues, I decided to publish my current version for everyone to see
(and update).

