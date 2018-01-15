# Deep Learning Images with docker
โปรเจคนี้เป็นโปรเจคที่ทำขึ้นเพื่อรวบรวม Library ที่ใช้งานบ่อยๆ ในงาน Deep Learning, Machine Learning เอามาใส่ไว้ใน Docker โดยทางเราได้เลือกที่จะใช้ **[Keras](https://keras.io/)** เป็น Framework และมี [Tensorflow](https://www.tensorflow.org/) เป็น Backend Framework

## ความต้องการของระบบ
เบื้องต้นเราได้ทำการทดสอบบน Ubuntu 16.04 with Docker version 17.12.0-ce, build c97c6d6 สามารถที่จะ Build Image นี้ได้ผ่าน โดยสเปคที่ทำการใช้งานเบื้องต้นนั้นเราได้กำหนดไว้ดังนี้

 - Ubuntu 16.04 LTS
 - Docker version 17.12.0-ce, build c97c6d6
 - Nvidia driver version 384.111
 - nvidia-docker (essential!)

ซึ่งหากคุณต้องการรัน Image นี้ คุณจำเป็นที่จะต้องมี [docker](https://www.docker.com/) engine ติดตั้งไว้อยู่ในเครื่องก่อนนะครับ
## วิธีการ Build Image นี้

via docker hub:

> coming soon.

via manual:

    git clone https://github.com/mynameismaxz/docker-deeplearning/
    cd docker-deeplearning
    git checkout master
    docker build -t $USER/docker-deeplearning:latest -f Dockerfile.gpu .
รอสักครู่ใหญ่ๆ ไปหากาแฟทานก่อน กลับมา Build Image เสร็จแล้วใช้งานได้เลยครับ ^_^

## วิธีการ RUN Image นี้
ทางเราได้ใช้งาน nvidia-docker ในการสร้าง Container ซึ่งทำให้สามารถใช้งาน Feature ของ nvidia ได้ใน Container โดยมีคำสั่งที่ใช้ในการรันดังนี้

    nvidia-docker run --name docker-deeplearning -v /path/to/your/project/:/workspace/ -p 6006:6006 -p 80:80 -p 8888:8888 -p 3000:3000 mynameismaxz/docker-deeplearning:latest

## พอร์ตที่ใช้งาน
|Port| Description  |
|--|--|
| 80 | for cloud9 ide |
| 3000 | for cloud9 ide |
| 6006 | for tensorboard(optional) |
| 8888 | for jupyter |


## ปัญหาและคำถาม

เมื่อคุณพบปัญหาต่างๆเกี่ยวกับ Image นี้สามารถสร้าง **issue** ไว้ให้ได้ ทางเราจะพยายามหาคำตอบให้เร็วที่สุดครับ
