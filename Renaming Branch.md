## 🔄 Rename Branch Lokal (belum di-push ke remote)

Jika kamu **belum push** branch tersebut, cukup lakukan:

```bash
git branch -m nama_lama nama_baru
```

Contoh:

```bash
git branch -m feat/123/login/improve-ui fix/123/login/fix-ui-bug
```

---

## 🔁 Rename Branch yang Sudah di-Push ke Remote

### 1. **Rename branch lokal:**

```bash
git branch -m nama_lama nama_baru
```

### 2. **Delete branch lama di remote:**

```bash
git push origin --delete nama_lama
```

### 3. **Push branch baru ke remote:**

```bash
git push origin nama_baru
```

### 4. **Set upstream (agar branch baru tracking remote):**

```bash
git push --set-upstream origin nama_baru
```

---

## ⚠️ Catatan Penting untuk Kolaborasi

* Setelah rename, orang lain yang sudah checkout branch lama **perlu rename lokal mereka** juga, atau delete branch lama mereka dan checkout ulang.
* Selalu komunikasikan rename ke tim lewat PR comment, Slack, atau Jira.

---

## ✅ Rangkuman

| Kondisi                  | Perintah                                                                                                     |
| ------------------------ | ------------------------------------------------------------------------------------------------------------ |
| Rename branch lokal saja | `git branch -m old_name new_name`                                                                            |
| Rename branch + remote   | `git branch -m`, `git push origin --delete old`, `git push origin new`, `git push --set-upstream origin new` |
| Orang lain mau update    | `git fetch --prune`, lalu `git branch -m old new` atau `git checkout origin/new -b new`                      |
