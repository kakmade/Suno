# SUNO Tuner

Two small browser tools for drafting prompts for Suno, so you waste fewer credits.
Dua alat kecil berbasis browser untuk menyusun prompt Suno, supaya kredit tidak terbuang.

| Tool | File |
|---|---|
| **Style Tuner**: builds the *Style of Music* prompt | <a href="suno-style-tuner.html">suno-style-tuner.html</a> |
| **Tags Tuner**: builds the lyric tags per section | <a href="suno-tags-tuner.html">suno-tags-tuner.html</a> |

[Bahasa Indonesia](#bahasa-indonesia) | [English](#english)

---

## Bahasa Indonesia

### Apa ini

Dua halaman HTML mandiri dengan slider dan kotak isian. Keduanya menghasilkan teks yang tinggal kamu salin ke Suno. Hasilnya memakai istilah musik (kebanyakan Italia) dengan terjemahan Inggris di bawahnya, karena dalam pengujian istilah musik lebih dipatuhi Suno daripada kalimat deskriptif yang panjang.

Konsepnya: **style prompt adalah cetak biru, tag di lirik adalah pelaksanaannya.** Style Tuner mengatur karakter keseluruhan lagu, Tags Tuner mengatur apa yang terjadi di tiap bagian lagu.

### Cara membuka

Klik tautan di tabel di atas untuk membuka alatnya di browser (Chrome, Safari, Firefox, dan sejenisnya). Tidak perlu instalasi. Tautannya relatif terhadap halaman, jadi bekerja di mana pun file ini dihosting (GitHub Pages, Vercel, dan sejenisnya).

Kalau yang terbuka hanya tampilan kode (misalnya saat README dibaca di GitHub), buka file-nya, pilih **Download raw file**, lalu buka file `.html` itu di browser.

### Cara pakai Style Tuner

1. Isi **Genre**: genre utama, genre kedua (dengan slider era), genre sentuhan (*slip*), dan genre pemecah (*rupture*). Kolom ini punya saran otomatis, tapi kamu bebas mengetik sendiri.
2. Atur slider: pengolahan dan suasana, tempo, nuansa (XY pad: gelap sampai terang, lemah sampai meledak), gaya duet, jenis suara pria dan wanita, drum, bass, dinamika instrumen, dan ritme.
3. Salin hasil dari kotak **Final Result** dengan tombol 📋.
4. Tempel ke kotak **Style of Music** di Suno.

Pola hasilnya kurang lebih: *(medium) (genre) in (tempo) tempo with (vokal)*, diikuti istilah instrumen lainnya.

### Cara pakai Tags Tuner

1. Di **Choose Instruments**, ketik instrumenmu: Primary, Secondary, Tertiary, Drums, dan Bass. Kolom dibiarkan kosong kalau tidak dipakai.
2. Kartu **Opening Break** selalu ada paling atas. Kalau ingin menentukan genre, mulai lirik dengan Break: ketik genre di kolom **Genre** (ada saran otomatis) dan, kalau perlu, beri modifier instrumen.
3. Di tiap kartu section berikutnya, pilih jenis section (Intro, Verse 1, Verse 2, Pre-Chorus, Chorus, Bridge, Build, Break, Drop, Solo, Instrumental, Interlude, Spoken, Outro).
4. Tekan chip instrumen yang ingin diberi modifier. Namanya terisi otomatis dari langkah 1.
5. Atur slider tiap instrumen: **Articulation**, **Density**, **Dynamics**, **Direction**. Semua slider mulai dari Off di sisi kiri. Centang **Tacet** untuk mendiamkan instrumen di section itu.
6. Untuk bagian ucapan, pilih **Spoken**: ketik teksnya lalu atur Delivery, Pace, dan Dynamics.
7. Tekan **+ Section** untuk menambah bagian lagu. Hasil tiap section ada di dalam kartunya (kotak kuning), salin dengan 📋.
8. Tempel ke kotak **Lyrics** di Suno, di atas lirik tiap bagian.

Format hasilnya:

```
[Break: bossa nova, guitar - muted sparso]

[Pre-Chorus: guitar - muted sparso pianissimo, viola - tremolo pianissimo]

[Chorus: guitar - legato sostenuto fortissimo, viola - sostenuto fortissimo]

[Spoken: sotto voce lento]
teks yang diucapkan di sini
```

Kotak output bisa diedit dengan tangan. Begitu kamu mengetik di dalamnya, pembaruan otomatis berhenti untuk section itu. Tekan **back to auto** untuk mengembalikannya.

### Temuan dari pengujian

- Tag **memengaruhi**, bukan memerintah. Hasilnya tidak 100% mengikuti, tapi jejaknya terdengar.
- Istilah musik Italia (misalnya *maestoso*, *con brio*) lebih berhasil daripada frasa Inggris yang panjang. Kata yang terlalu panjang untuk hal yang singkat membuat Suno berjalan sendiri.
- Menulis angka BPM membuat Suno terpaku di kisaran itu pada generasi berikutnya, jadi tempo ditulis dengan istilah.
- Hi-hat dan cymbal tidak dipatuhi, sehingga tidak disediakan. Kick, snare, dan groove hanya berfungsi sebagai acuan kasar.
- Tag Density (misalnya *Tenuto*, *Sostenuto*, *Sparso*) membantu menahan Suno dari permainan virtuoso atau arpeggio yang terlalu ramai.
- Untuk menentukan genre, mulai lirik dengan Break.
- Hindari koma di dalam style prompt karena Suno bisa mencampuradukkannya.

### Disclaimer

- Ini alat bantu **tidak resmi** dan **tidak berafiliasi** dengan Suno. Suno adalah merek dagang pemiliknya masing-masing.
- Alat ini hanya membantu menyusun teks. **Tidak ada jaminan** hasil lagu yang sesuai harapan. Suno dapat berubah perilakunya kapan saja, dan hasil tiap generasi bisa berbeda.
- Kamu bertanggung jawab atas penggunaan Suno dan lagu yang dihasilkan, termasuk mengikuti ketentuan layanan Suno.
- Semua berjalan di browsermu. Alat ini tidak mengirim data apa pun ke server.
- Disediakan apa adanya (*as is*), tanpa garansi dalam bentuk apa pun.

---

## English

### What is this

Two standalone HTML pages with sliders and input fields. Both produce text you copy straight into Suno. The output uses music terminology (mostly Italian) with an English translation below it, because in testing Suno followed music terms better than long descriptive sentences.

The concept: **the style prompt is the blueprint, and the lyric tags are the execution.** The Style Tuner sets the overall character of the song, the Tags Tuner controls what happens in each section.

### How to open

Click a link in the table above to open the tool in your browser (Chrome, Safari, Firefox and so on). No installation needed. The links are relative to the page, so they work wherever this file is hosted (GitHub Pages, Vercel and so on).

If only the code view opens (for example when reading this README on GitHub), open the file, choose **Download raw file**, then open the `.html` file in a browser.

### How to use the Style Tuner

1. Fill in **Genre**: primary genre, secondary genre (with an era slider), accent genre (*slip*), and rupture genre. These fields offer suggestions, but you can type anything.
2. Set the sliders: processing and atmosphere, tempo, nuance (XY pad: dark to bright, weak to explosive), duet style, male and female voice types, drums, bass, instrument dynamics, and rhythm.
3. Copy the result from the **Final Result** box with the 📋 button.
4. Paste it into Suno's **Style of Music** box.

The result follows roughly this pattern: *(medium) (genre) in (tempo) tempo with (vocal)*, followed by the remaining instrument terms.

### How to use the Tags Tuner

1. Under **Choose Instruments**, type your instruments: Primary, Secondary, Tertiary, Drums and Bass. Leave a field empty if you do not use it.
2. The **Opening Break** card is always on top. To set the genre, start your lyrics with a Break: type a genre in the **Genre** field (with autocomplete) and optionally add instrument modifiers.
3. In each following section card, pick the section type (Intro, Verse 1, Verse 2, Pre-Chorus, Chorus, Bridge, Build, Break, Drop, Solo, Instrumental, Interlude, Spoken, Outro).
4. Tap the chips of the instruments you want to give modifiers. Their names are filled in from step 1.
5. Set each instrument's sliders: **Articulation**, **Density**, **Dynamics**, **Direction**. Every slider starts at Off on the left. Tick **Tacet** to silence an instrument in that section.
6. For spoken passages, choose **Spoken**: type the text, then set Delivery, Pace and Dynamics.
7. Press **+ Section** to add a part of the song. Each section's result sits inside its own card (the yellow box), copy it with 📋.
8. Paste into Suno's **Lyrics** box, above the lyrics of each part.

Output format:

```
[Break: bossa nova, guitar - muted sparso]

[Pre-Chorus: guitar - muted sparso pianissimo, viola - tremolo pianissimo]

[Chorus: guitar - legato sostenuto fortissimo, viola - sostenuto fortissimo]

[Spoken: sotto voce lento]
the spoken text goes here
```

The output box can be edited by hand. Once you type in it, auto-updating stops for that section. Press **back to auto** to restore it.

### Findings from testing

- Tags **influence**, they do not command. Results do not follow them 100%, but traces are audible.
- Italian music terms (for example *maestoso*, *con brio*) work better than long English phrases. Using long wording for something short makes Suno go its own way.
- Writing a BPM number makes Suno stay stuck in that range on later generations, so tempo is written as a term.
- Hi-hat and cymbals are not obeyed, so they are not offered. Kick, snare and groove only work as a rough reference.
- Density tags (such as *Tenuto*, *Sostenuto*, *Sparso*) help keep Suno from overly busy virtuoso or arpeggio playing.
- To set the genre, start your lyrics with a Break.
- Avoid commas inside the style prompt, because Suno may mix them up.

### Disclaimer

- These are **unofficial** helper tools and are **not affiliated** with Suno. Suno is a trademark of its respective owner.
- The tools only help you draft text. There is **no guarantee** of any particular musical result. Suno may change its behavior at any time, and every generation can differ.
- You are responsible for your use of Suno and the songs you generate, including following Suno's terms of service.
- Everything runs in your browser. The tools do not send any data to a server.
- Provided "as is", without warranty of any kind.
