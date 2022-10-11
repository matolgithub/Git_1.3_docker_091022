FROM python:3.10.6

LABEL maintainer="matol 888888@888.ru"
 
ENV TZ=Europe/Moscow

WORKDIR /my-project

COPY ./ /my-project

RUN pip install --upgrade pip

RUN pip install -r /my-project/stocks_products/requirements.txt

ENV SECRET_KEY django-insecure-nw^y+m^wmxza1asgk+)!ua2qx9)g+#v=6%76-9i8i(6eqiw94j

ENV DEBUG True

WORKDIR /my-project/stocks_products

RUN python3 manage.py migrate

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "stocks_products.wsgi"]