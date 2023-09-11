FROM weibeld/ubuntu-networking

# Create the /home/danny directory
RUN mkdir -p /home/danny && \
    chmod 755 /home/danny

RUN apt-get update && apt-get install -y python3 openssh-server wget && \
    echo 'CSEC{L00k_Mum_1_4m_4_H4ck3r}' > /home/danny/flag1.txt && \
    echo 'flag 3 CSEC{R3v3r3e_P0rt_F0rw4rd_g0_Brr}' > /index.html

COPY server.py /server.py

RUN useradd -m -d /home/danny -s /bin/bash danny && \
    echo 'danny:danny' | chpasswd

RUN chmod 400 /index.html /server.py

RUN sed -i 's/.*PasswordAuthentication.*/PasswordAuthentication yes/' /etc/ssh/sshd_config && \
    service ssh restart

CMD ["sleep", "1d"]
