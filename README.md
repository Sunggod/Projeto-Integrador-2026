# Projeto Integrador 2026

## Nossa proposta

Estamos criando um site e um aplicativo para facilitar a rotina de quem usa e administra quadras esportivas. Quem joga poderá assistir a recortes das partidas e agendar horários. Já quem administra poderá organizar os agendamentos e acompanhar as métricas da quadra.

## Nosso diferencial

Vamos usar inteligência artificial para gerar recortes de jogadas. Também queremos oferecer um agendamento simples e bem desenvolvido, que pode se tornar uma das principais funcionalidades da plataforma.

## Tecnologias

- Linguagem: TypeScript 6
- Banco de dados: Prisma ORM
- Web: Next.js com TypeScript
- Mobile: Expo e React Native
- Visão computacional: MediaPipe Tasks Vision

## Configuração inicial

Para começar, precisamos ter Node.js e npm instalados. Na raiz do projeto, criamos os aplicativos web e mobile com estes comandos:

```bash
npx create-next-app@latest web --ts
npx create-expo-app@latest mobile --template blank-typescript
```

### Web

No aplicativo web, instalamos as dependências do Prisma e do MediaPipe Tasks Vision:

```bash
cd web
npm install @prisma/client @mediapipe/tasks-vision
npm install -D prisma typescript@^6
npx prisma init
```

Depois de configurar a conexão com o banco de dados e o modelo em `prisma/schema.prisma`, criamos a primeira migração:

```bash
npx prisma migrate dev --name init
npx prisma generate
```

### Mobile

```bash
cd mobile
npm install -D typescript@^6
```

No aplicativo mobile, esse comando instala o TypeScript.

## Executar em desenvolvimento

Para trabalhar localmente, iniciamos cada aplicativo em um terminal separado:

```bash
cd web
npm run dev
```

```bash
cd mobile
npx expo start
```
