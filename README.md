# Baby Board — pages légales

Les deux pages publiques exigées par la Google Play Console pour l'application
Baby Board :

- [`privacy.html`](privacy.html) — politique de confidentialité ;
- [`account-deletion.html`](account-deletion.html) — procédure de suppression de compte.

Elles vivent dans un dépôt public séparé parce que Google doit pouvoir les
ouvrir sans compte et sans installer l'application, alors que le dépôt de
l'application est privé. Aucun code de l'application ne se trouve ici.

Elles ont d'abord été servies par une Edge Function Supabase, ce qui ne marche
pas : le portail Supabase réécrit toute réponse HTML en `text/plain` et y
ajoute une CSP `sandbox`, si bien que la page s'affiche en code source au lieu
d'être rendue.

La source de vérité du texte de la politique de confidentialité reste
`PRIVACY_POLICY.md` dans le dépôt de l'application ; toute modification doit
être répercutée ici.
