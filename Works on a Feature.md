# Penjelasan

Dalam pengoperasian git tim besar yang sudah dijelaskan, bisa saja terdapat beberapa branch untuk setiap fitur. Untuk itu kita perlu membersihkan branch-branch tersebut ketika sudha merge.

## Mengecek branch merge atau belum
```bash
git checkout develop
git pull origin develop   # pastikan develop terbaru
git branch --merged | grep 'feat/123/login'
git log --oneline|grep "adjust"
```

## Working with team
Kita bisa saja bekerja dengan tim dalam sebuah fitur. Untuk itu, kita perlu membuat branch fitur pada remote origin agar bisa kolaborasi online.

## Auto-clean Branch Fitur di Remote
Jika kamu izinkan push branch fitur ke origin, kamu bisa:
- Setup aturan di GitHub/GitLab agar branch yang sudah merged ke develop otomatis dihapus.
- Gunakan bot/script untuk delete remote branch setelah merge selesai.