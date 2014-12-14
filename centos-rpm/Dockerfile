FROM centos:centos7

#必要ソフトウェアのインストール
RUN yum install -y yum-utils

#キーの登録
RUN rpm --import "https://pgp.mit.edu/pks/lookup?op=get&search=0x3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF"

#リポジトリの登録
RUN yum-config-manager --add-repo http://download.mono-project.com/repo/centos/

#monoのインストール
RUN yum install -y mono-devel fsharp mono-vbnc nuget

#monoで使用するSSL証明書のインストール
RUN mozroots --machine --import --sync --quiet

