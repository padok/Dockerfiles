FROM debian:stretch-slim

RUN apt-get update && apt-get install -y \
    biber \
    latexmk \
    make \
    texlive-full \
    # Latexindent
    git \
    perl \
    liblog-log4perl-perl \
    liblog-dispatch-perl-perl \
    libyaml-tiny-perl \
    libnamespace-autoclean-perl \
    libspecio-perl \
    libeval-closure-perl \
    libparams-validationcompiler-perl \
    libfile-homedir-perl \
    libunicode-linebreak-perl \
    && rm -rf /var/lib/apt/lists/*

RUN cd root; \
    git clone https://github.com/cmhughes/latexindent.pl.git; \
    rm /usr/bin/latexindent; \
    ln -s /root/latexindent.pl/latexindent.pl /usr/bin/latexindent


