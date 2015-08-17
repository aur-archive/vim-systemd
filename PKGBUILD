# Maintainer: Jason St. John <jstjohn .. purdue . edu>

pkgname=vim-systemd
pkgver=20110915
pkgrel=2
pkgdesc="Vim syntax highlighting for systemd unit files"
arch=('any')
url="http://fedorapeople.org/cgit/wwoods/public_git/vim-scripts.git/"
license=('unknown')
depends=('vim')
source=("syntax-systemd.vim::http://fedorapeople.org/cgit/wwoods/public_git/vim-scripts.git/plain/syntax/systemd.vim"
        "ftdetect-systemd.vim::http://fedorapeople.org/cgit/wwoods/public_git/vim-scripts.git/plain/ftdetect/systemd.vim"
        '0001-Add-more-syntax-keywords-for-service-and-socket-file.patch')
sha512sums=('9774a1479b9fe2da5fc3e34e9ec5d768508df90f04740e41b4a36bc1ec909a1e7be01951878aa16d34a83c4c955089a2bb9fd5c04910cc85a88a3f164de2cf6a'
            'b622456290f6b7adf4e4da5c24d6bd5200078c28c833aa357775482299f7e252beabf36a6de8ecfac16ecae0c7491e78541813e6c444bd2ce3f9376bae6fed8f'
            'e60024eb86b7089580956fcd57a2a2e618f737eff7c9f59a55f29817c38d904b1fe9603b3465963414ba6dcccd305627f0d63177aee9bf00fa7399bdc5ee5b69')

package() {
	cd "$srcdir"

	# Patch submitted upstream but not applied in Git tree
	patch --follow-symlinks < "$srcdir/0001-Add-more-syntax-keywords-for-service-and-socket-file.patch"

	install -Dm644 syntax-systemd.vim "$pkgdir/usr/share/vim/vimfiles/syntax/systemd.vim"
	install -Dm644 ftdetect-systemd.vim "$pkgdir/usr/share/vim/vimfiles/ftdetect/systemd.vim"
}
