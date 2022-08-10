# ShalihRizal-ShalihRizaldy-Tugas2

----Bugs----
1. Variable _score yang tidak ada di GameManager.cs [low]
2. Variable score yang bertipe int di-assign kedalam text [Very High]
3. Game sudah berjalan bahkan sebelum tombol play ditekan [High]
4. Plane masih terjatuh setelah countdown berakhir [Very High]  
5. Plane malah lebih kebawah saat diklik [Very High]  
6. Plane masih melaju bahkan setelah menabrak Obstacle [Very High] 
7. Penempatan tombol play menimpa text judul game [Low] 
8. Highscore belum berfungsi [Low]





----Approach----
1. Mengubah variable _score --> score
2. Mengubah statement scoretext.text = score menjadi scoretext.text = score.ToString();
3. Menambahkan CountdownText.OnCountdownFinished += OnCountdownFinished; pada OnEnabled() di GameManager.cs dan mengubah return value dari bool gameover menjadi true
4. Mengaktifkan script dan collider pada plane dan mengubah bool !gameover --> gameover
5. Mengubah rigidbody.AddForce (Vector2.down* tapForce, ForceMode2D.Force); menjadi rigidbody.AddForce (Vector2.up * tapForce, ForceMode2D.Force);
6. Mengubah tag dari prefab woods yg bagian bottom menjadi "DeadZone" dan mengubah kesalahan penulisan tag "DeadZones" --> "DeadZone"
7. Saya pindahkan
8. Mengubah operator < menjadi > di GameManager.cs
