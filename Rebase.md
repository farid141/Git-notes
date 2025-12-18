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
pick b2c3d4e Fixed bug      ← biarkan ini tetap pick (ganti commit desc jika perlu)
squash c3d4e5f Another trial
squash d4e5f6g Final working version   
```

Dengan cara diatas, commit `c3d` dan `d4e5` dihapus, tetapi perubahan akan tetap ada di `b2c3d`.

## Drop

Jika menggunakan `drop` maka commit dan perubahan akan dihapus. (sangat jarang digunakan).
