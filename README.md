# gerrit
gerrit


install php 7.4.10

Je start met maken van project
composer create-project symfony/website-skeleton the_spacebar 4.4.*

composer insall

Installerd de Doctrine
composer req orm

Je maakt server aan
composer req server

maakt de templaats aan
composer req twig 

insalller de bootstrap
composer req twbs/bootstrap
uit vendor bootstrap de js en css in public zetten
<link href="assets/css/bootstrap.min.css" rel="stylesheet">
<script type="text/javascript" src="assets/js/bootstrap.min.js"></script>

Hier installer je security
composer req security

intallerd de router
composer req router

Installerd de router
composer req annotations

Je installert form
composer req form

maak je database aan
php bin/console doctrine:database:create


Maakt gebriker aan
php bin/console make:user


Maakt login form en controller
php bin/console make:auth

php bin/console security:encode-password

voor de roles
config/packeges/security.yaml


$roles = $token->getRoleNames();
if (in_array("ROLE_ADMIN", $roles)){
    return new RedirectResponse($this->urlGenerator->generate('default'));
}
