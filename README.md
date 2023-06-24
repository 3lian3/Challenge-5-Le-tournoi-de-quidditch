# Challenge-5-Le-tournoi-de-quidditch

SELECT wizard.firstname, wizard.lastname, player.role, team.name
FROM player
JOIN wizard ON wizard.id = player.wizard_id
JOIN team ON team.id = player.team_id
ORDER BY team.name, player.role, wizard.lastname, wizard.firstname;

SELECT wizard.lastname, wizard.firstname, player.role
FROM player
JOIN wizard ON wizard.id = player.wizard_id
WHERE player.role = 'seeker'
ORDER BY wizard.lastname, wizard.firstname;

SELECT wizard.lastname, wizard.firstname, player.role
FROM player
JOIN wizard ON wizard.id = player.wizard_id
WHERE player.id IS NULL
