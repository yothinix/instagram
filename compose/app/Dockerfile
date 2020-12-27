FROM python:3.9

ENV APPLICATION_ROOT /app/
RUN mkdir $APPLICATION_ROOT

COPY ./requirements/ $APPLICATION_ROOT/requirements
COPY ./compose/app/entrypoint-local.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

WORKDIR $APPLICATION_ROOT

RUN pip install -r requirements/local.txt

COPY . $APPLICATION_ROOT