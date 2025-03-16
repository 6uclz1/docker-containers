FROM danteev/texlive:latest

WORKDIR /workspace

# 日本語フォントとcurlを追加
RUN apt-get update && apt-get install -y fonts-noto-cjk curl

# tlmgrを最新に更新し、必要なパッケージをインストール
RUN curl -fsSL -o /tmp/update-tlmgr-latest.sh https://mirror.ctan.org/systems/texlive/tlnet/update-tlmgr-latest.sh && \
    chmod +x /tmp/update-tlmgr-latest.sh && \
    sh /tmp/update-tlmgr-latest.sh && \
    tlmgr update --self && \
    tlmgr install latexmk uplatex dvipdfmx bxjscls
