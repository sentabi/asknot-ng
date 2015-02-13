# asknot-ng -- edisi Bantuan Fedora-ID

Ditulis oleh [@ralphbean][threebean]. Terinspirasi dari [wcidfm] oleh [Josh Matthews][jdm], [Henri Koivuneva][wham],
dan [lainnya][asknot-contribs].

Modifikasi ini lebih fleksibel dari versi awalnya. Script utama,
``asknot-ng.py``, berfungsi seperti *static-site generator*. Inputnya
terdiri dari tiga hal:

- File pertanyaan, ditulis dalam yaml (lihat
  [contoh][example-questions]) atau [file pertanyaan
  Fedora][fedora-questions]). Untuk situs Bantuan Fedora-ID gunakan
  [file pertanyaan Bantuan][fedora-id-bantuan].
- File template, ditulis dalam mako (template
  [default][default-template] seharusnya bisa dipakai semua orang).
- Perintah 'theme' digunakan untuk memilih file css yang akan dipakai.

Untuk melihat hasil program ini, bisa melihat [situs versi Fedora][wcidff].

## Cara untuk Berkontribusi

* [Belajar pakai Git dan GitHub][github-help]
* [Pedoman forking dan pull request][patches]

Untuk mempermudah alur kerja, disarankan membuat feature branch yang
berdasarkan branch `develop-id`, dan mengirim pull request setelah
siap. Tolong melakukan rebase sesering mungkin untuk memastikan karya
Anda dapat di-merge balik secara mudah!

## Pasang Dan Jalankan

Clone kode sumber dari repo

```
$ git clone https://github.com/fedora-id/asknot-ng.git
$ cd asknot-ng
```
Pasang Python PIP
```
su -c "dnf install python-pip"
```

Pasang pustaka yang dibutuhkan

```
$ pip install -r requirements.txt
```

Jalankan

```
$ ./asknot-ng.py templates/index.html questions/bantuan.yml --theme fedora
$ xdg-open asknot.html
```

[threebean]: http://threebean.org
[fedora]: http://getfedora.org
[example-questions]: https://github.com/fedora-infra/asknot-ng/blob/develop/questions/example.yml
[fedora-questions]: https://github.com/fedora-infra/asknot-ng/blob/develop/questions/fedora.yml
[default-template]: https://github.com/fedora-infra/asknot-ng/blob/develop/templates/index.html
[github-help]: https://help.github.com/articles/good-resources-for-learning-git-and-github/
[requirements]: https://github.com/fedora-infra/asknot-ng/blob/develop/requirements.txt
[patches]: https://help.github.com/articles/editing-files-in-another-user-s-repository/
[wcidfm]: http://whatcanidoformozilla.org
[wcidff]: http://whatcanidoforfedora.org
[jdm]: http://www.joshmatthews.net
[wham]: http://wham.fi
[asknot-contribs]: https://github.com/jdm/asknot/contributors