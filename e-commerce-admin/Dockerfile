FROM node:20.5.1-alpine
RUN mkdir -p /app
WORKDIR /app
COPY package.json .   # Copia el package.json desde el directorio raíz
RUN npm cache clean --force
RUN npm install
COPY . .              # Copia los demás archivos desde el directorio raíz
RUN npx prisma generate ./prisma/schema.prisma
EXPOSE 3000
ENTRYPOINT ["npm", "run", "dev"]
