# Gestão de Empréstimos — app iOS (e Android)

## O que mudou no código
- Nova tela de **configuração inicial** (pede URL + API Key do Supabase, e opcionalmente chave/proxy da IA). Testa a conexão e, se já houver backup na nuvem, oferece carregá-lo.
- Tailwind e Chart.js agora são **locais** (pasta `www/vendor`), então o app abre sem depender de CDN.

## Gerar o app iOS (precisa de um Mac com Xcode)
1. Instale Node.js 18+ e Xcode.
2. Na pasta do projeto:  `npm install`  e depois  `npm run ios`
3. No Xcode: Signing & Capabilities → escolha seu Team (Apple ID) → conecte o iPhone → ▶ Run.
   - Apple ID gratuito: o app expira em 7 dias.
   - Conta Apple Developer (US$ 99/ano): instala por mais tempo, TestFlight e App Store.
4. Alterou o HTML? Rode `npm run sync` e rode de novo no Xcode.

## Android (APK), se quiser
`npm run android` → Android Studio → Build > Build APK(s).

## Sem Mac?
Hospede a pasta `www` (Netlify/Vercel/GitHub Pages) → abra no Safari → Compartilhar → **Adicionar à Tela de Início**. Vira um app em tela cheia, de graça.
