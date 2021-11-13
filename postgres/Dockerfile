FROM postgres:alpine
WORKDIR /usr/src/tag_parser
COPY tag_parser .
RUN set -exu; \
	apk add --no-cache --virtual .build-deps \
		llvm11-dev \
		clang \
		g++ \
		make; \
	make install; \
	apk del --no-network .build-deps;

ENV POSTGRES_DB=watame_db
ENV POSTGRES_PASSWORD=password123
ENV POSTGRES_USER=watame
CMD ["postgres"]
