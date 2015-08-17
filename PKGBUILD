# Contributor: Alexsandr Pavlov <kidoz at mail dot ru>
pkgname=ruby-debug-base19x
_gemname=${pkgname}
pkgver=0.11.30.pre10
pkgrel=2
pkgdesc="Fast implementation of the standard Ruby debugger debug.rb."
arch=('i686' 'x86_64')
url="https://github.com/ruby-debug/ruby-debug-base19"
license=('MIT')
depends=('ruby' 'rubygems' 'ruby-columnize' 'ruby-linecache19' 'ruby-ruby_core_source' 'ruby-source')
source=(http://rubygems.org/downloads/${_gemname}-${pkgver}.gem)
noextract=(${_gemname}-${pkgver}.gem)
md5sums=('7ae6ba9ba9a9766fe8d73b55548dddfd')

build() {
  cd "${srcdir}"
  export HOME=/tmp
  local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"
  gem install --no-user-install --ignore-dependencies -i "${pkgdir}${_gemdir}" ${_gemname}-${pkgver}.gem -- --with-ruby-include=/usr/src/ruby-1.9.3-p194
}
