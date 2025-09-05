# 1) Añade todo (incluye los no rastreados)
git add -A

# 2) Fija fecha pasada (CDMX UTC-06:00)
$env:GIT_AUTHOR_DATE = "2025-09-12 11:00:00 -0600"
$env:GIT_COMMITTER_DATE = $env:GIT_AUTHOR_DATE

# 3) Crea el commit
git commit -m "mensaje"

# 4) Limpia variables
Remove-Item Env:\GIT_AUTHOR_DATE, Env:\GIT_COMMITTER_DATE

# 5) Sube
git push
