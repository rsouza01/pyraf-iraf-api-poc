# FROM tepickering/iraf-community-base:latest
FROM ghcr.io/rsouza01/iraf-community-base:0.5

ARG USER_ID=developer
ARG GROUP_ID=developer

RUN adduser --home /home/${USER_ID} ${USER_ID}

RUN passwd -d ${USER_ID}

RUN groupadd -f iraf && useradd -g iraf iraf
RUN mkdir -p /home/iraf && chown -R iraf:iraf /home/iraf

USER iraf
ENV HOME /home/iraf
ENV USER iraf