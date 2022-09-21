# Pip Package Install - Universal Docker mod

Using this mod you can install any Pip package during startup by providing it through the environment variable `INSTALL_PIP_PACKAGES`. This is then passed into the pip command as such: `pip install ...`.

In any docker container arguments, set an environment variable `DOCKER_MODS=linuxserver/mods:universal-pip-package-install`

If adding multiple mods, enter them in an array separated by `|`, such as
`DOCKER_MODS=linuxserver/mods:universal-pip-package-install|linuxserver/mods:universal-stdout-logs`.
Similarly, for installing multiple packages separate them by `|`. E.g., to
install `beetcamp`, and `beets-follow` add the following lines to your docker
compose service:

```yaml
- DOCKER_MODS=linuxserver/mods:universal-pip-package-install
- INSTALL_PIP_PACKAGES=beetcamp|beets-follow ```
