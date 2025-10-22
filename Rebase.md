# Rebase

Merupakan cara untuk membersihkan commit, dimana kita ingin commit dihapus tetapi tetap ada perubahan di commit sekarang.

>git rebase -i HEAD~N

```bash
# Muncul seperti ini
pick a1b2c3d First attempt
pick b2c3d4e Fixed bug
pick c3d4e5f Another trial
pick d4e5f6g Final working version


# Ubah menjadi 
pick a1b2c3d First attempt
squash b2c3d4e Fixed bug
squash c3d4e5f Another trial
pick d4e5f6g Final working version   ← biarkan ini tetap pick
```

Dengan cara diatas, commit `b2c` dan `c3d` dihapus, tetapi perubahan akan tetap ada di final version.

Tetapi jika menggunakan `drop` maka commit dan perubahan akan dihapus.
