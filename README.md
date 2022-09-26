<h1> Git, GitHub & GitHub Desktop </h1>
<p> oleh Felix Irwanto (GameDev Kelompok 3) </p>
<br>

## Git

<p align="center"><img width="100%" src="https://user-images.githubusercontent.com/113922230/192131506-96631995-546e-414e-a47f-fee6fc331e28.png"></p>

<b><a href="https://git-scm.com/">Git</a></b> adalah perangkat lunak manajemen sumber koding yang berguna untuk mencatat setiap perubahan (bahkan hingga perubahan satu huruf) menjadi berbagai versi hingga dapat mengembangkan koding secara bersama tanpa harus saling menunggu (non-linear manner). 

Istilah-istilah yang ada pada Git:
- Repository: Tempat / folder penyimpanan khusus yang terdiri dari beberapa versi history yang ditampung pada suatu tempat. Terdapat dua tempat penyimpanan yaitu di server dan di lokal. Dengan menyimpan di repo, maka setiap orang dalam projek dapat meng-clone (mendowndload semua versi history yang ada pada projek tersebut).
- Push: Diibaratkan upload ke Github
- Commit: Diibaratkan membuat save point, komitmen dari perubahan yang ada di projek
- Pull: Diibaratkan download ke laptop. Bedanya dengan clone, pull hanya mendownload file yang hanya merupakan commit terakhir.
- Branch: Bagian dari main repository yang memiliki history yang berbeda dengan master dan bisa dijadikan satu dengan master atau main branch asal latest history nya sama, jika latest perubahannya tidak sama maka biasanya akan terjadi conflict.

## GitHub

<p align="center"><img width="100%" src="https://user-images.githubusercontent.com/113922230/192134062-fef79c66-9c73-4889-bda7-4b2dfb9aa73e.png"></p>

<b><a href="https://github.com/">GitHub</a></b> adalah salah satu penyedia layanan Git, juga terdapat aplikasi lain penyedia layanan Git, yaitu [GitLab](https://about.gitlab.com/), [Plastic SCM](https://www.plasticscm.com/), namun layanan ini kalah populer.

Tahapan untuk melakukan Commit Pertama dengan GitHub:
- Membuat akun di [GitHub](https://github.com/) 
- Buka Command Line di dir folder yang diinginkan
- git add -A
- git add README.md
- git commit -m "first commit"
- git branch -M main
- git remote add origin git@github.com:username/nama-project
- git push -u origin main

## GitHub Desktop

<p align="center"><img width="50%" src="https://user-images.githubusercontent.com/113922230/192211617-04cf0ea3-f4f2-4861-94c5-4ae7d5902ee2.png"></p>

<b><a href="https://desktop.github.com/">GitHub Desktop</a></b> adalah layanan GUI dari GitHub yang menyederhanakan alur kerja pengembangan git. Penggunaan GitHub Desktop tidak terdapat pemakaian syntax git.

Referensi cara melakukan push, pull, dan commit di GitHub Desktop:
1. Commit Pertama:
- Membuat akun di [GitHub](https://github.com/) 
- Download <a href="https://desktop.github.com/">GitHub Desktop</a>
- Atur File > Option > Accounts > Sign In
- Atur File > Option > Git > Atur nama & Pilih Email yang ingin dipakai

<p align="center"><img width="100%" src="https://user-images.githubusercontent.com/113922230/192140781-e2d57c9d-d9a4-4aee-942a-b52e64e6c460.png"></p>

- Pilih Create a New Repo from Hard Drive dan isi identitasnya
- Otomatis terbuat initial commit
- Publish repository

2. Clone Project: 

<p align="center"><img width="100%" src="https://user-images.githubusercontent.com/113922230/192140706-3964f674-ac32-4e3f-921a-e6681204059a.png"></p>

- Sumber pribadi: File > Clone Repo > GitHub.com > Pilih sumber & projek yang mau diclone
- Sumber publik: File > Clone Repo > URL > Pilih sumber & projek yang mau diclone (projek milik orang yang bersifat publik)

3. Push:
- Setelah ada perubahan, akan tampak di Changes
- Pilih branch sumber tempat untuk push
- Isi pesan singkat pada Summary
- Isi pesan deskriptif pada Description (opsional)
- Commit
- Push origin

4. Pull:
- Pada Visual Studio Code, Pilih branch sumber tempat untuk pull
- Tekan titik tiga, lalu pull

5. Merge: Terjadi ketika mengedit sumber file yang sama, namun di push ke lebih dari satu branch yang berbeda
- Pada GitHub Desktop, pindah ke main
- Tekan "Choose a branch to merge into main"

<p align="center"><img width="100%" src="https://user-images.githubusercontent.com/113922230/192139517-6d47c14c-0591-415d-9bda-9c208bda66bb.png"></p>

- Pilih branch yang mau digabung
- Lalu, tekan Create a merge commit
- Push origin
- Terkadang bisa terjadi conflict

6. Conflict: Sering terjadi ketika merge file, untuk menyelesaikannya harus menggunakan Visual Studio Code (VSC) atau Command Line (GitHub Desktop belum support perbaikan secara langsung).

<p align="center"><img width="100%" src="https://user-images.githubusercontent.com/113922230/192139345-795acfb2-3e3d-4edd-b03f-532bc0b95663.png"></p>

- Setelah buka di VSC, dapat dilihat beberapa perbedaan, pilih Accept Current Change (progress dari HEAD), Accept Incoming Change (progress dari branch), atau Both Change (progress dari kedua file)
- Setelah resolve, klik continue merge
- Push origin

7. Pull Request (mirip dengan merge, bedanya online langsung mengubah di remote):
- Buat Branch baru yang diisikan coding

<p align="center"><img width="100%" src="https://user-images.githubusercontent.com/113922230/192139749-00e50472-3d5a-4139-b685-27525089e0ee.png"></p>

- Pada VSC, tekan "Compare & Pull Request"
- Terkadang bisa juga terjadi conflict
- Kemudian isi pesan dan komen pull request, serta tekan "Create pull request"
- Jika projek individu, dapat langsung confirm merge
- Jika projek memiliki beberapa collaborator, harus disetujui salah satu collaborator lain baru dapat melakukan merge.

Catatan Tambahan:

<p align="center"><img width="100%" src="https://user-images.githubusercontent.com/113922230/192134468-5dea02cc-2d38-4602-a7f1-48ee3d7c8919.png"></p>

<b><a href="https://git-scm.com/">Git Graph</a></b> adalah ekstensi tambahan di Visual Studio COde (VSC) yang berfungsi membantu melacak history commit dari sebuah projek. 

<b><a href="https://gist.github.com/takekazuomi/10955889">Git Ignore</a></b> adalah file tambahan di projek yang berfungsi mengabaikan beberapa file seperti settingan pribadi dan log projek agar tidak ikut terupload ke git. 

<br/>
**Copyright by Felix Irwanto - 2022**
