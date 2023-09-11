FROM weibeld/ubuntu-networking

RUN mkdir -p /home/jack && \
    chmod 755 /home/jack

RUN apt-get update && apt-get install -y python3 openssh-server wget && \
    echo 'CSEC{1m_Wh3r3_Th3_4dm1N5_4r3}' > /home/jack/flag4.txt && \
    echo 'flag 5 CSEC{P0rt_F0rw4rd1ng_4nd_P1v0t1ng_Pr0}' > /index.html

COPY server.py /server.py

RUN chmod 400 /index.html /server.py

RUN useradd -m -d /home/jack -s /bin/bash jack && \
    echo 'jack:Complexpassword123#' | chpasswd

CMD ["sleep", "1d"]
