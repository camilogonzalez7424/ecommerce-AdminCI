FROM node:20.5.1-alpine
RUN mkdir -p /app
WORKDIR /app
COPY . .
RUN npm cache clean --force
RUN npm install
RUN npx prisma generate ./prisma/schema.prisma
EXPOSE 3000
ENTRYPOINT ["npm", "run", "dev"]

# Agregar el siguiente comando al final del Dockerfile para verificar el contenido del directorio /app
RUN ls -la /app
