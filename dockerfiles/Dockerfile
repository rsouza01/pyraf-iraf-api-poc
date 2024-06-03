# FROM tepickering/iraf-community-base:latest
FROM ghcr.io/rsouza01/iraf-community-base:0.4

ARG USER_ID=developer
ARG GROUP_ID=developer


RUN adduser \
    --home /home/${USER_ID} \
    --password "" \
    ${USER_ID}

RUN groupadd -f -g ${GROUP_ID} iraf && \
    useradd -l -u ${USER_ID} -g iraf iraf

RUN mkdir -p /home/iraf && chown -R iraf:iraf /home/iraf

USER iraf
ENV HOME /home/iraf