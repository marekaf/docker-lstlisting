# docker-lstlisting

How to use it:

```
\begin{lstlisting}[language=docker-compose-2,caption={Example docker-compose.yml},breaklines=true,label={code:compose}]
version: '2'
services:
  web:
     build: .
     ports:
        - "5000:5000"
     volumes:
        - .:/code
        - logvolume01:/var/log
     links:
        - redis
  redis:
     image: redis
volumes:
    logvolume01: {}
\end{lstlisting}
```
