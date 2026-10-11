# SUNO Tuner

Two small browser tools for drafting prompts for Suno, so you waste fewer credits.
Dua alat kecil berbasis browser untuk menyusun prompt Suno, supaya kredit tidak terbuang.

| Tool | File |
|---|---|
| **Style Tuner**: builds the *Style of Music* prompt | [suno-style-tuner.html](suno-style-tuner.html) |
| **Tags Tuner**: builds the lyric tags per section | [suno-tags-tuner.html](suno-tags-tuner.html) |

[Bahasa Indonesia](#bahasa-indonesia) | [English](#english)

---

## Bahasa Indonesia

### Apa ini

Dua halaman HTML mandiri dengan slider dan kotak isian. Keduanya menghasilkan teks yang tinggal kamu salin ke Suno. Hasilnya memakai istilah musik (kebanyakan Italia) dengan terjemahan Inggris di bawahnya, karena dalam pengujian istilah musik lebih dipatuhi Suno daripada kalimat deskriptif yang panjang.

Konsepnya: **style prompt adalah cetak biru, tag di lirik adalah pelaksanaannya.** Style Tuner mengatur karakter keseluruhan lagu, Tags Tuner mengatur apa yang terjadi di tiap bagian lagu.

### Cara membuka

1. Klik nama file di tabel di atas, lalu pilih **Download raw file**.
2. Buka file `.html` itu di browser (Chrome, Safari, Firefox, dan sejenisnya). Tidak perlu instalasi atau koneksi khusus.

Kalau repositori ini memakai GitHub Pages, kamu juga bisa membukanya langsung dari alamat Pages-nya.

### Cara pakai Style Tuner

1. Isi **Genre**: genre utama, genre kedua (dengan slider era), genre sentuhan (*slip*), dan genre pemecah (*rupture*). Kolom ini punya saran otomatis, tapi kamu bebas mengetik sendiri.
2. Atur slider: pengolahan dan suasana, tempo, nuansa (XY pad: gelap sampai terang, lemah sampai meledak), gaya duet, jenis suara pria dan wanita, drum, bass, dinamika instrumen, dan ritme.
3. Salin hasil dari kotak **Final Result** dengan tombol 📋.
4. Tempel ke kotak **Style of Music** di Suno.

Pola hasilnya kurang lebih: *(medium) (genre) in (tempo) tempo with (vokal)*, diikuti istilah instrumen lainnya.

### Cara pakai Tags Tuner

1. Di **Choose Instruments**, ketik instrumenmu: Primary, Secondary, Tertiary, Drums, dan Bass. Kolom dibiarkan kosong kalau tidak dipakai.
2. Di tiap kartu section, pilih jenis section (Intro, Verse 1, Verse 2, Pre-Chorus, Chorus, Bridge, Build, Break, Drop, Solo, Instrumental, Interlude, Spoken, Outro).
3. Tekan chip instrumen yang ingin diberi modifier. Namanya terisi otomatis dari langkah 1.
4. Atur slider tiap instrumen: **Articulation**, **Density**, **Dynamics**, **Direction**. Semua slider mulai dari Off di sisi kiri. Centang **Tacet** untuk mendiamkan instrumen di section itu.
5. Untuk bagian ucapan, pilih **Spoken**: ketik teksnya lalu atur Delivery, Pace, dan Dynamics.
6. Salin hasil per section dengan 📋, atau semuanya sekaligus dengan **Copy all**.
7. Tempel ke kotak **Lyrics** di Suno, di atas lirik tiap bagian.

Format hasilnya:

```
[Pre-Chorus: Guitar - Muted Sparso Pianissimo, Viola - Tremolo Pianissimo]

[Chorus: Guitar - Legato Sostenuto Fortissimo, Viola - Sostenuto Fortissimo]

[Spoken: Sotto voce Lento]
teks yang diucapkan di sini
```

Kotak output bisa diedit dengan tangan. Begitu kamu mengetik di dalamnya, pembaruan otomatis berhenti untuk section itu. Tekan **back to auto** untuk mengembalikannya. Tombol **copy previous** menyalin pengaturan section sebelumnya.

### Temuan dari pengujian

- Tag **memengaruhi**, bukan memerintah. Hasilnya tidak 100% mengikuti, tapi jejaknya terdengar.
- Istilah musik Italia (misalnya *maestoso*, *con brio*) lebih berhasil daripada frasa Inggris yang panjang. Kata yang terlalu panjang untuk hal yang singkat membuat Suno berjalan sendiri.
- Menulis angka BPM membuat Suno terpaku di kisaran itu pada generasi berikutnya, jadi tempo ditulis dengan istilah.
- Hi-hat dan cymbal tidak dipatuhi, sehingga tidak disediakan. Kick, snare, dan groove hanya berfungsi sebagai acuan kasar.
- Tag Density (misalnya *Tenuto*, *Sostenuto*, *Sparso*) membantu menahan Suno dari permainan virtuoso atau arpeggio yang terlalu ramai.
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

1. Click a file name in the table above, then choose **Download raw file**.
2. Open the `.html` file in any browser (Chrome, Safari, Firefox and so on). No installation or special setup needed.

If this repository uses GitHub Pages, you can also open the tools straight from its Pages address.

### How to use the Style Tuner

1. Fill in **Genre**: primary genre, secondary genre (with an era slider), accent genre (*slip*), and rupture genre. These fields offer suggestions, but you can type anything.
2. Set the sliders: processing and atmosphere, tempo, nuance (XY pad: dark to bright, weak to explosive), duet style, male and female voice types, drums, bass, instrument dynamics, and rhythm.
3. Copy the result from the **Final Result** box with the 📋 button.
4. Paste it into Suno's **Style of Music** box.

The result follows roughly this pattern: *(medium) (genre) in (tempo) tempo with (vocal)*, followed by the remaining instrument terms.

### How to use the Tags Tuner

1. Under **Choose Instruments**, type your instruments: Primary, Secondary, Tertiary, Drums and Bass. Leave a field empty if you do not use it.
2. In each section card, pick the section type (Intro, Verse 1, Verse 2, Pre-Chorus, Chorus, Bridge, Build, Break, Drop, Solo, Instrumental, Interlude, Spoken, Outro).
3. Tap the chips of the instruments you want to give modifiers. Their names are filled in from step 1.
4. Set each instrument's sliders: **Articulation**, **Density**, **Dynamics**, **Direction**. Every slider starts at Off on the left. Tick **Tacet** to silence an instrument in that section.
5. For spoken passages, choose **Spoken**: type the text, then set Delivery, Pace and Dynamics.
6. Copy each section with 📋, or everything at once with **Copy all**.
7. Paste into Suno's **Lyrics** box, above the lyrics of each part.

Output format:

```
[Pre-Chorus: Guitar - Muted Sparso Pianissimo, Viola - Tremolo Pianissimo]

[Chorus: Guitar - Legato Sostenuto Fortissimo, Viola - Sostenuto Fortissimo]

[Spoken: Sotto voce Lento]
the spoken text goes here
```

The output box can be edited by hand. Once you type in it, auto-updating stops for that section. Press **back to auto** to restore it. **Copy previous** duplicates the previous section's settings.

### Findings from testing

- Tags **influence**, they do not command. Results do not follow them 100%, but traces are audible.
- Italian music terms (for example *maestoso*, *con brio*) work better than long English phrases. Using long wording for something short makes Suno go its own way.
- Writing a BPM number makes Suno stay stuck in that range on later generations, so tempo is written as a term.
- Hi-hat and cymbals are not obeyed, so they are not offered. Kick, snare and groove only work as a rough reference.
- Density tags (such as *Tenuto*, *Sostenuto*, *Sparso*) help keep Suno from overly busy virtuoso or arpeggio playing.
- Avoid commas inside the style prompt, because Suno may mix them up.

### Disclaimer

- These are **unofficial** helper tools and are **not affiliated** with Suno. Suno is a trademark of its respective owner.
- The tools only help you draft text. There is **no guarantee** of any particular musical result. Suno may change its behavior at any time, and every generation can differ.
- You are responsible for your use of Suno and the songs you generate, including following Suno's terms of service.
- Everything runs in your browser. The tools do not send any data to a server.
- Provided "as is", without warranty of any kind.
