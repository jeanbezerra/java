### Ferramentas gerais

```sh
sudo apt update && sudo apt full-upgrade -y && \
sudo apt install -y \
  openjdk-25-jdk \
  openjdk-25-dbg \
  openjdk-25-source \
  maven \
  gradle \
  git \
  git-lfs \
  openssh-client \
  curl \
  wget \
  ca-certificates \
  gnupg \
  unzip \
  zip \
  tar \
  gzip \
  xz-utils \
  build-essential \
  gcc \
  g++ \
  make \
  cmake \
  pkg-config \
  gdb \
  valgrind \
  strace \
  ltrace \
  htop \
  sysstat \
  procps \
  lsof \
  tree \
  file \
  jq \
  yq \
  vim \
  nano \
  less \
  rsync \
  ripgrep \
  fd-find \
  iproute2 \
  iputils-ping \
  dnsutils \
  net-tools \
  netcat-openbsd \
  traceroute \
  tcpdump \
  socat \
  telnet \
  openssl \
  shellcheck \
  && sudo apt autoremove -y \
  && sudo apt clean \
  && git lfs install
```

### JAVA_HOME global

```sh
sudo tee /etc/profile.d/JAVA_HOME.sh > /dev/null <<'EOF'
export JAVA_HOME=/usr/lib/jvm/java-25-openjdk-amd64
export PATH="$JAVA_HOME/bin:$PATH"
EOF
```

```sh
sudo chmod 644 /etc/profile.d/JAVA_HOME.sh
source /etc/profile.d/JAVA_HOME.sh
```
