FROM node:10

WORKDIR app/
COPY . .

RUN npm install && \
    rm -rf /var/lib/apt/lists/* && \ 
    useradd -m app && \ 
    chown -R app /app/
    
USER app 

CMD ["npm", "start"]
