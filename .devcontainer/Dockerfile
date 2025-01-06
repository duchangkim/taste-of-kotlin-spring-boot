FROM mcr.microsoft.com/devcontainers/java:17

# 사용자 생성 (sudo 권한 포함)
RUN useradd -m -s /bin/bash -G sudo developer && \
    echo "developer ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

# Gradle 캐시 설정
RUN mkdir -p /home/developer/.gradle && \
    chown -R developer:developer /home/developer/.gradle

USER developer

RUN git config --global user.name "duchangkim" && \
    git config --global user.email "duchangkim.dev@gmail.com" \
