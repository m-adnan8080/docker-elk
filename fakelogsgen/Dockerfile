FROM python:2

ENV TZ=Asia/Karachi
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

WORKDIR /usr/src/app

COPY requirements.txt ./
RUN pip install --no-cache-dir --upgrade pip
RUN pip install --no-cache-dir -r requirements.txt

COPY apache-fake-log-gen.py .

ENTRYPOINT [ "python", "./apache-fake-log-gen.py" ]
CMD [ "" ]
