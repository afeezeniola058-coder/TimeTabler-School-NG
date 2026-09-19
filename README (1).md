# TimeTabler-School-NG - Secure Cloud SaaS

Polytechnic & Secondary School Timetable Generator with Cloud Save.

Live Demo: (Add your Vercel URL after deploy)

## Features
- ✅ Institution Type: Polytechnic / Secondary
- ✅ Level, Arms/Groups, Subject/Teacher/Room assignment
- ✅ Intelligent Generation (no clash, even distribution)
- ✅ Master / Class-wise / Teacher-wise / Room-wise views
- ✅ Drag to reschedule with conflict detection + Find Best Alternative + Undo
- ✅ Tap to move (mobile friendly)
- ✅ Cloud Save with Supabase (private to each school)
- ✅ No backend exposed to users - secure

## How Schools Use It
1. Open app → Sign Up with email
2. Load Demo or add your own Departments/Teachers/Subjects/Rooms
3. Click Generate Master Timetable
4. View results: Master / Class-wise / Teacher-wise / Room-wise
5. Drag any session to move - app checks conflicts automatically
6. Check saved results: 💾 View Saved Data → Cloud tab
7. Open on any device - Sign In → timetable restores

## Tech Stack
- Frontend: React + Tailwind (single HTML file)
- Backend: Supabase (Postgres + Auth + RLS)
- Hosting: Vercel
- No build step needed - just deploy index.html

## Admin Access (Owner Only)
Normal users see clean app with no backend.
To see diagnostics, add ?admin=true to URL:
```
https://your-domain.vercel.app?admin=true
```

## Supabase Setup (Already done for this project)
Project: https://npotjqrumvavotwxfnog.supabase.co

Tables:
- profiles (id, email, institution_name)
- timetables (user_id, institution_type, name, departments, teachers, subjects, rooms, hours, timetables_data)

RLS enabled - users can only see their own timetables.

## Deploy to Vercel
1. Push this repo to GitHub as TimeTabler-School-NG
2. Vercel → New Project → Import repo
3. Deploy - no config needed
4. Done!

## Security
- Supabase anon key is in frontend (safe, RLS protected)
- Service role key NEVER in frontend
- Backend panel hidden from public - only ?admin=true shows it
- Each school's data isolated by auth.uid() = user_id policy

---
Built by Hafiz Ennyhorlar - TimeTabler School NG v3.0 SaaS Final
