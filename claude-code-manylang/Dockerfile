FROM rockylinux:9
RUN dnf update -y && dnf install -y wget git make vim g++ cmake
RUN cd ~ && curl -O https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh && bash ~/Miniconda3-latest-Linux-x86_64.sh -b -p /miniconda3 && rm -f ~/Miniconda3-latest-Linux-x86_64.sh && source /miniconda3/bin/activate && conda init --all
RUN cd ~ && curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.4/install.sh | bash && \. "$HOME/.nvm/nvm.sh" && nvm install 24 && corepack enable yarn && corepack prepare yarn@stable --activate
ENV http_proxy="http://host.docker.internal:7890"
ENV https_proxy="http://host.docker.internal:7890"
RUN curl -fsSL https://claude.ai/install.sh | bash 

CMD ["bash"]
