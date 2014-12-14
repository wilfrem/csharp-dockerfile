FROM ubuntu:trusty

#curlのインストール
RUN apt-get update && apt-get install -y curl && rm -rf /var/lib/apt/lists/*

#aptに鍵を登録
RUN apt-key adv --keyserver pgp.mit.edu --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF

#monoのリポジトリを登録し、aptからmonoをインストール
RUN echo "deb http://download.mono-project.com/repo/debian wheezy main" | sudo tee /etc/apt/sources.list.d/mono-xamarin.list && apt-get update && apt-get install -y mono-devel fsharp mono-vbnc nuget && rm -rf /var/lib/apt/lists/*

#monoで使用するSSL証明書のインストール
RUN mozroots --machine --import --sync --quiet

