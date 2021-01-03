ARG VARIANT="latest"
FROM elixir:${VARIANT}

ARG USERNAME=vscode
ARG USER_UID=1000

RUN apt update \
    && apt install -y sudo \
    && useradd -s /bin/bash --uid ${USER_UID} -m ${USERNAME} \
    && echo "${USERNAME} ALL=(root) NOPASSWD:ALL" > /etc/sudoers.d/vscode \
    && chmod 0440 /etc/sudoers.d/vscode
