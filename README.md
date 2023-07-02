# dockerfile "Hello Netology"

* ### Dockerfile
---
FROM continuumio/miniconda3:latest

COPY app/1.sh /app/1.sh

RUN chmod +x app/1.sh

RUN conda install python

RUN pip install mlflow boto3 pymysql

EXPOSE 8080

CMD ["bash", "app/1.sh"]

---

* ### 1.sh
---
#!/bin/bash

echo "Hello Netology"

---

* ### log
---
![image](https://github.com/MSRaith/dockerfile_hello_word/assets/89347252/2766e43d-2dc5-499a-b54f-5be61c87a982)

---
