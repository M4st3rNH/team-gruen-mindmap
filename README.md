# Team Grün · Mindmap

Gemeinsame Produktideen-Mindmap für **Team Grün**.

**Live:** https://m4st3rnh.github.io/team-gruen-mindmap/

## Architektur

- **GitHub Pages** stellt nur die statische Weboberfläche bereit.
- **Supabase Auth** übernimmt die Anmeldung.
- **Supabase PostgreSQL + RLS** speichern und schützen den gemeinsamen Mindmap-Stand.
- **Supabase Storage** enthält Bilder und Anhänge in einem privaten Bucket.
- Zugriff auf Projektdaten erhalten nur freigeschaltete Mitglieder der `team_gruen_members`-Allowlist.

## Sicherheit

Der im Browser verwendete Supabase Publishable Key ist für Client-Anwendungen vorgesehen.  
**Keine Secret-/Service-Role-Keys in dieses Repository eintragen.**

Die Zugriffsrechte werden serverseitig durch Supabase Auth und Row Level Security erzwungen.

## Veröffentlichung

Die Seite wird automatisch über GitHub Actions zu GitHub Pages veröffentlicht, sobald GitHub Pages im Repository unter **Settings → Pages → Source: GitHub Actions** aktiviert wurde.

---
Team Grün
