# [![DebOps logo][debops-logo]](https://debops.org/) DebOps Contrib

*Your Debian-based data center in a box*

[debops-logo]: https://raw.githubusercontent.com/debops/debops/master/lib/images/debops-small.png

The DebOps project provides a set of general-purpose [Ansible][ansible] roles
that can be used to manage [Debian][debian] or [Ubuntu][ubuntu] hosts. In
addition, a default set of Ansible playbooks can be used to apply the provided
roles in a controlled way, using Ansible inventory groups.

[ansible]: https://github.com/ansible/ansible/
[debian]: https://www.debian.org/
[ubuntu]: https://www.ubuntu.com/

This repository contains an additional set of Ansible roles that are not part
of the "core" DebOps project. It is an equivalent of the Debian `contrib`
archive section. Roles in this repository install and manage non-free or
commercial software and use different DebOps roles as dependencies.

At the moment the repository is not integrated with the main DebOps project. To
use it, you can clone the repository to your machine and symlink the roles and
playbooks to the DebOps "project directory".


## Licensing

The DebOps project is licensed under the [GNU General Public License 3.0][gpl-3.0].
You can find full text of the license in the [LICENSE][license] file.

[gpl-3.0]: https://www.gnu.org/licenses/gpl-3.0
[license]: https://github.com/debops/debops-contrib/blob/master/LICENSE
