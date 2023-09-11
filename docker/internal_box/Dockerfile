FROM weibeld/ubuntu-networking

RUN mkdir -p /home/ariana && \
    chmod 755 /home/ariana


RUN apt-get update && apt-get install -y python3 openssh-server wget && \
    echo 'CSEC{1m_0v3r_H3r3_N0w}' > /home/ariana/flag2.txt

RUN useradd -m -d /home/ariana -s /bin/bash ariana && \
    echo 'ariana:Password1' | chpasswd

CMD ["sleep", "1d"]
