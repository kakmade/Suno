# SUNO V6+ Tuner

Two small browser tools for drafting prompts for Suno V6+, so you waste fewer credits.
Dua alat kecil berbasis browser untuk menyusun prompt Suno V6+, supaya kredit tidak terbuang.

| Tool | Open |
|---|---|
| **Style Tuner**: builds the *Style of Music* prompt | [Open the Style Tuner](https://kakmade.github.io/Suno/suno-style-tuner.html) |
| **Tags Tuner**: builds the lyric tags per section | [Open the Tags Tuner](https://kakmade.github.io/Suno/suno-tags-tuner.html) |

[Bahasa Indonesia](#bahasa-indonesia) | [English](#english)

---

## Bahasa Indonesia

### Apa ini

Dua halaman dengan slider dan kotak isian, dibuka langsung lewat tautan di tabel di atas. Keduanya menghasilkan teks yang tinggal kamu salin ke Suno. Hasilnya memakai istilah musik (kebanyakan Italia) dengan terjemahan Inggris di bawahnya, karena dalam pengujian istilah musik lebih dipatuhi Suno daripada kalimat deskriptif yang panjang.

Konsepnya: **style prompt adalah cetak biru, tag di lirik adalah pelaksanaannya.** Style Tuner mengatur karakter keseluruhan lagu, Tags Tuner mengatur apa yang terjadi di tiap bagian lagu.

### Cara pakai Style Tuner

1. Isi kartu **Genre**:
   - **Primary**: genre dasar lagu.
   - **Secondary**: genre kedua, dengan empat pilihan cara masuk (lihat di bawah) dan slider **Era** untuk menempelkan dekade padanya.
   - **Accent (slip)** dan **Rupture**: sentuhan genre yang makin kuat. Slip adalah selipan singkat, rupture lebih tinggi dari slip.
   - Kolom genre punya saran otomatis, tapi kamu bebas mengetik sendiri. Secondary, slip, dan rupture boleh dikosongkan.
2. Pilih cara genre kedua masuk:
   - **Influenced**: memengaruhi, terasa di birama.
   - **Weight**: memberi bobot, terasa di cara instrumen dimainkan.
   - **Colored**: meminjam instrumen khas genre itu.
   - **Mixed**: genre kedua berpeluang masuk di salah satu bagian lagu (verse, bridge, break, chorus, dan lainnya).
3. Atur kartu dan slider lainnya:
   - **Processing & Atmosphere**, **EQ & Amplifier**, dan **Layer** untuk karakter rekaman dan suara.
   - **Tempo** (opsional: centang **Include BPM number** kalau angkanya mau ikut masuk) dan **Nuance** (XY pad: gelap sampai terang, lemah sampai meledak).
   - **Instrumental**: centang untuk mematikan semua pilihan vokal. Hasilnya diganti kata *instrumental*.
   - **Duet Style**, serta **Male** dan **Female**: jenis suara, emosi, dan tarikan vokal. Centang **Featuring** untuk gang vocals, group singing, atau sing-along.
   - **Drum** (kick, snare, groove), **Bassline**, **Instrument Dynamics**, dan **Rhythm**.
   - Slider yang bisa dimatikan punya posisi **Off** (ikon ❌) di tengah, dan semuanya mulai dari Off.
4. Mau coba kombinasi acak? Tekan **🎲 Surprise Me**. Tombol ini menimpa semua pilihan yang sedang aktif, kecuali centang Instrumental dan Include BPM number.
5. Salin **Final Result (Music Terminology)** dengan tombol 📋. Itu yang paling mendekati hasil yang diharapkan. Versi **Final Result (English)** di bawahnya adalah terjemahannya.
6. Tempel ke kotak **Style of Music** di Suno.

Pola hasilnya kurang lebih: *(medium) (genre) in (tempo) tempo with (vokal) vocal*, diikuti istilah instrumen lainnya. Pola genre:

- *G1 influenced with G2*
- *G1 with G2 weight*
- *G1 colored with G2*
- *G1 mixed with G2*

Setelahnya bisa ditambah *and G3 slip* dan *and G4 rupture*. Bagian vokal bisa diakhiri *featuring ...* (dipisah koma kalau lebih dari satu).

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

### Style dan tag: pembagian peran

- Isi **Style Tuner** ke kolom *Style of Music*. Itu saran yang ditafsirkan Suno dengan longgar.
- Isi **Tags Tuner** ke kolom *Lyrics*. Tag lebih berwenang, jadi hal yang harus dipatuhi (misalnya instrumen yang harus diam di satu bagian, atau bagian mana yang dimasuki genre kedua) lebih cocok dikerjakan lewat tag.

### Temuan dari pengujian

- Tag **memengaruhi**, bukan memerintah. Hasilnya tidak 100% mengikuti, tapi jejaknya terdengar.
- Istilah musik Italia (misalnya *maestoso*, *con brio*) lebih berhasil daripada frasa Inggris yang panjang. Kata yang terlalu panjang untuk hal yang singkat membuat Suno berjalan sendiri.
- Menulis angka BPM bisa membuat Suno terpaku di kisaran itu pada lagu berikutnya, jadi tempo secara bawaan ditulis dengan istilah. Angka BPM hanya ikut kalau kamu mencentangnya.
- Pada genre kedua, **influenced with** terasa di birama, sedangkan **weight** terasa di cara instrumen dimainkan.
- Hi-hat dan cymbal tidak dipatuhi, sehingga tidak disediakan. Kick, snare, dan groove hanya berfungsi sebagai acuan kasar.
- Tag Density (misalnya *Tenuto*, *Sostenuto*, *Sparso*) membantu menahan Suno dari permainan virtuoso atau arpeggio yang terlalu ramai.
- Hindari koma di dalam style prompt karena Suno bisa mencampuradukkannya. Satu pengecualian adalah daftar setelah *featuring*, yang memang memakai koma.

### Disclaimer

- Ini alat bantu **tidak resmi** dan **tidak berafiliasi** dengan Suno. Suno adalah merek dagang pemiliknya masing-masing.
- Alat ini hanya membantu menyusun teks, supaya kredit tidak terbuang. **Tidak ada jaminan** hasil lagu yang sesuai harapan. Suno dapat berubah perilakunya kapan saja, dan hasil tiap generasi bisa berbeda.
- Kamu bertanggung jawab atas penggunaan Suno dan lagu yang dihasilkan, termasuk mengikuti ketentuan layanan Suno.
- Semua berjalan di browsermu. Alat ini tidak mengirim data apa pun ke server.
- Disediakan apa adanya (*as is*), tanpa garansi dalam bentuk apa pun.

---

## English

### What is this

Two pages with sliders and input fields, opened straight from the links in the table above. Both produce text you copy into Suno. The output uses music terminology (mostly Italian) with an English translation below it, because in testing Suno followed music terms better than long descriptive sentences.

The concept: **the style prompt is the blueprint, and the lyric tags are the execution.** The Style Tuner sets the overall character of the song, the Tags Tuner controls what happens in each section.

### How to use the Style Tuner

1. Fill in the **Genre** card:
   - **Primary**: the base genre of the song.
   - **Secondary**: a second genre, with four ways of entering (see below) and an **Era** slider that attaches a decade to it.
   - **Accent (slip)** and **Rupture**: genre touches of increasing strength. A slip is a brief touch, a rupture is stronger than a slip.
   - The genre fields offer suggestions, but you can type anything. Secondary, slip and rupture can be left blank.
2. Choose how the secondary genre comes in:
   - **Influenced**: shapes the song, felt in the meter.
   - **Weight**: adds weight, felt in how the instruments are played.
   - **Colored**: borrows the signature instruments of that genre.
   - **Mixed**: the secondary genre may show up in any part of the song (verse, bridge, break, chorus and so on).
3. Set the other cards and sliders:
   - **Processing & Atmosphere**, **EQ & Amplifier** and **Layer** for the recording and sound character.
   - **Tempo** (optional: tick **Include BPM number** to add the number to the result) and **Nuance** (XY pad: dark to bright, weak to explosive).
   - **Instrumental**: tick it to turn off all vocal options. The result then says *instrumental*.
   - **Duet Style**, plus **Male** and **Female**: voice type, emotion and vocal pull. Tick **Featuring** for gang vocals, group singing or sing-along.
   - **Drum** (kick, snare, groove), **Bassline**, **Instrument Dynamics** and **Rhythm**.
   - Sliders that can be turned off have an **Off** position (❌) in the middle, and all of them start at Off.
4. Want a random combination? Press **🎲 Surprise Me**. It overwrites everything currently selected, except the Instrumental and Include BPM number ticks.
5. Copy **Final Result (Music Terminology)** with the 📋 button. That is the one that gets closest to the expected result. **Final Result (English)** below it is the translation.
6. Paste it into Suno's **Style of Music** box.

The result follows roughly this pattern: *(medium) (genre) in (tempo) tempo with (vocal) vocal*, followed by the remaining instrument terms. The genre patterns are:

- *G1 influenced with G2*
- *G1 with G2 weight*
- *G1 colored with G2*
- *G1 mixed with G2*

You can follow with *and G3 slip* and *and G4 rupture*. The vocal part can end with *featuring ...* (comma separated when there is more than one).

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

### Style and tags: who does what

- Put the **Style Tuner** output in the *Style of Music* field. It is a suggestion that Suno interprets loosely.
- Put the **Tags Tuner** output in the *Lyrics* field. Tags carry more authority, so anything that must be obeyed (for example an instrument that has to stay silent in one part, or which part the secondary genre enters) is better done with tags.

### Findings from testing

- Tags **influence**, they do not command. Results do not follow them 100%, but traces are audible.
- Italian music terms (for example *maestoso*, *con brio*) work better than long English phrases. Using long wording for something short makes Suno go its own way.
- Writing a BPM number can make Suno stay stuck in that range on later songs, so tempo is written as a term by default. The number is only added when you tick it.
- On the secondary genre, **influenced with** shows up in the meter, while **weight** shows up in how the instruments are played.
- Hi-hat and cymbals are not obeyed, so they are not offered. Kick, snare and groove only work as a rough reference.
- Density tags (such as *Tenuto*, *Sostenuto*, *Sparso*) help keep Suno from overly busy virtuoso or arpeggio playing.
- Avoid commas inside the style prompt, because Suno may mix them up. The one exception is the list after *featuring*, which does use commas.

### Disclaimer

- These are **unofficial** helper tools and are **not affiliated** with Suno. Suno is a trademark of its respective owner.
- The tools only help you draft text, so you do not waste credits. There is **no guarantee** of any particular musical result. Suno may change its behavior at any time, and every generation can differ.
- You are responsible for your use of Suno and the songs you generate, including following Suno's terms of service.
- Everything runs in your browser. The tools do not send any data to a server.
- Provided "as is", without warranty of any kind.
