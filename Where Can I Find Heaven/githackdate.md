# 1) Añade todo (incluye los no rastreados)
git add -A

# 2) Fija fecha pasada (CDMX UTC-06:00), the date is YYYY-MM-DD HH:MM:SS -0600
$env:GIT_AUTHOR_DATE = "2025-11-03 11:00:00 -0600"
$env:GIT_COMMITTER_DATE = $env:GIT_AUTHOR_DATE

# 3) Crea el commit
git commit -m "Where Can I Find Heaven"

# 4) Limpia variables
Remove-Item Env:\GIT_AUTHOR_DATE, Env:\GIT_COMMITTER_DATE

# 5) Sube
git push
