# FROM tepickering/iraf-community-base:latest
FROM ghcr.io/rsouza01/iraf-community-base:0.4

ENV USER_ID developer
ENV GROUP_ID developer

RUN groupadd -f -g ${GROUP_ID} iraf && \
    useradd -l -u ${USER_ID} -g iraf iraf

RUN mkdir -p /home/iraf && chown -R iraf:iraf /home/iraf

USER iraf
ENV HOME /home/iraf