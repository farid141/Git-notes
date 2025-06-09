Mengoperasikan git di tim besar:
- MASTER
- STAGING
- DEVELOP

## ada fitur baru
1. sync MASTER local dengan origin
2. buat branch baru dari master local dengan format
action(feat, UI, fix)/card(nomor kartu jira)/page(area)/desc(detail)
3. buat commit di branch tersebut
4. push origin sesuai nama branch tersebut
5. maintainer/senior akan merge ke DEVELOP


Beberapa branch yang butuh ada di local repo
- master (track origin/master)
- staging (track origin/staging, jika dibutuhkan)
- develop (track origin/develop)
- Hanya branch fitur yang aktif saat ini (belum merge)