FROM archlinux

# Sort mirrors by speed
RUN pacman --sync --refresh --noconfirm \
        reflector \
    && reflector \
        --save /etc/pacman.d/mirrorlist \
        --protocol https \
        --latest 20 \
        --sort rate

RUN yes | pacman --sync --refresh \
        ansible \
        ansible-lint \
        diffutils \
        docker \
        docker-compose \
        git \
        graphviz \
        helm \
        kubectl \
        kustomize \
        libisoburn \
        make \
        mdbook \
        p7zip \
        python \
        python-netaddr \
        terraform \
        zsh

CMD [ "/bin/zsh" ]
