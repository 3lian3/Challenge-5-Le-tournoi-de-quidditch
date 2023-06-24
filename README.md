# Challenge-5-Le-tournoi-de-quidditch

# Retourne les noms, prénoms, rôle et équipe de tous les joueurs, classés dans l’ordre alphabétique par équipe, puis par rôle dans l’équipe, puis par nom de famille, puis par prénom.

SELECT wizard.firstname, wizard.lastname, player.role, team.name
FROM player
JOIN wizard ON wizard.id = player.wizard_id
JOIN team ON team.id = player.team_id
ORDER BY team.name, player.role, wizard.lastname, wizard.firstname;

# Retourne uniquement les prénoms et noms des joueurs ayant le rôle de seeker (attrapeur), classés par ordre alphabétique de nom puis prénom

SELECT wizard.lastname, wizard.firstname, player.role
FROM player
JOIN wizard ON wizard.id = player.wizard_id
WHERE player.role = 'seeker'
ORDER BY wizard.lastname, wizard.firstname;

# Retourne la liste de tous les sorciers qui ne pratiquent pas le quidditch.

SELECT wizard.lastname, wizard.firstname, player.role
FROM player
JOIN wizard ON wizard.id = player.wizard_id
WHERE player.id IS NULL
