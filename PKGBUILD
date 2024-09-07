# Maintainer: Brian Thompson <brianrobt@pm.me>

pkgname=python-descript-audiotools
_srcname='audiotools'
pkgver=0.7.3
pkgrel=1
pkgdesc='Object-oriented handling of audio data, with GPU-powered augmentations, and more'
arch=('x86_64')
url="https://github.com/descriptinc/$_srcname"
license=('MIT')
depends=(
  'python-argbind'
  'python-numpy'
  'python-soundfile'
  # 'python-pyloudnorm'
  'python-importlib_resources'
  'python-scipy'
  'python-pytorch'
  'julius'
  'python-torchaudio'
  'python-ffmpy'
  'ipython'
  'python-rich'
  'python-matplotlib==3.5'
  'python-librosa'
  # 'python-pystoi'
  # 'python-torch_stoi'
  'python-flatten-dict'
  'python-markdown2'
  # 'python-randomname'
  'protobuf>=3.9.2' 'protobuf<3.20'
  'tensorboard'
  'python-tqdm'
)
makedepends=('python-wheel' 'python-build' 'python-installer')
checkdepends=(
  'python-pytest'
  'python-pytest-cov'
  'python-lineprofiler'
  # 'python-pesq'
  'python-gradio==3.32.0'
  'python-transformers>=4.23.1'
)
source=("https://github.com/descriptinc/$_srcname/archive/refs/tags/$pkgver.tar.gz")
sha512sums=('61bde301c53e8e01cbfa39b83a71fc596357b2ec3f53e14eaa422d74237baa9e630ef3ce251500956140e8dec44a8c2072153642f5fa7fafb909c2d083bfb1b9')

build() {
  cd $_srcname-$pkgver
  python -m build --wheel --no-isolation
}

package() {
  cd $_srcname-$pkgver
  python -m installer --destdir="$pkgdir" dist/*.whl
}
