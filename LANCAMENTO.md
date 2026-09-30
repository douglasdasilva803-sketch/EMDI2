# Lançamento do site — EMDI Higienização

Pasta pronta para publicar. Estrutura:

- `index.html` — o site
- `privacidade.html` — política de privacidade (LGPD)
- `assets/img/` — imagens otimizadas (WebP), favicon e imagem de compartilhamento
- `robots.txt` e `vercel.json` — configurações de indexação, cache e segurança

---

## 1. Publicar na Vercel (sem instalar nada)

1. Crie uma conta gratuita no **GitHub** (github.com) e outra na **Vercel** (vercel.com). Na Vercel, entre usando a conta do GitHub.
2. No GitHub, clique em **New repository**. Nome sugerido: `emdi-site`. Pode ser **Private**. Crie.
3. Na página do repositório, clique em **uploading an existing file** e arraste **todo o conteúdo desta pasta** (index.html, privacidade.html, robots.txt, vercel.json e a pasta assets). Clique em **Commit changes**.
4. Na Vercel: **Add New… → Project → Import** o repositório `emdi-site`. Não mude nenhuma configuração (Framework: **Other**). Clique em **Deploy**.
5. Em cerca de 1 minuto o site estará no ar em um endereço provisório como `emdi-site.vercel.app`.

Para atualizar no futuro: substitua o arquivo no GitHub (Upload files) e a Vercel publica sozinha.

## 2. Domínio próprio (ex.: emdihigienizacao.com.br)

1. Verifique a disponibilidade em **registro.br** e registre **no CPF ou CNPJ do dono da EMDI**.
2. Na Vercel: projeto → **Settings → Domains → Add** e digite o domínio.
3. A Vercel mostra os registros de DNS necessários. No registro.br, em **DNS** do domínio, cadastre exatamente esses registros (ou troque os servidores DNS para os da Vercel, se ela oferecer essa opção).
4. Aguarde a propagação (de minutos a algumas horas). O certificado de segurança (https) é criado automaticamente.
5. Depois, avise para eu ativar no código o endereço oficial (canonical e og:url) e gerar o `sitemap.xml`.

## 3. Medição (Google Analytics 4)

1. Acesse **analytics.google.com**, crie a conta **EMDI Higienização** e uma propriedade web com o endereço do site.
2. Copie o **ID de métricas** (formato `G-XXXXXXXXXX`).
3. No `index.html`, procure `var GA_ID='G-XXXXXXXXXX'` e troque pelo ID real (ou me envie o ID).
4. Com o ID ativo, o aviso de cookies aparece automaticamente. Nada é medido antes do "Aceitar".
5. Eventos que o site já envia:
   - `whatsapp_clique` (origem: conversa_guiada, montador_orcamento, rodape, conversa_direto) → **marque como evento principal (conversão)** em Administrador → Eventos
   - `conversa_aberta`, `conversa_assunto`, `conversa_objetivo`
   - `orcamento_item_adicionado`, `servico_girado`, `cta_clique`, `avaliacoes_google`

## 4. Google Search Console

1. Acesse **search.google.com/search-console** e adicione a propriedade do domínio.
2. Verifique pelo registro TXT de DNS (no registro.br) ou pela meta tag (há um espaço marcado no `index.html`).
3. Envie o `sitemap.xml` (gero quando o domínio estiver definido).

## 5. Perfil da Empresa no Google

Use o perfil que já tem as avaliações. Pontos para revisar:

- **Site:** colocar o endereço do novo site.
- **Área de atendimento:** Grande São Paulo (cidades e bairros atendidos).
- **Categoria principal:** procure por "limpeza de estofados" e escolha a opção mais próxima. Categorias adicionais: estética automotiva / limpeza automotiva.
- **Serviços:** higienização de sofás, colchões, cadeiras, poltronas, estofados automotivos; impermeabilização; estética automotiva; lavagem detalhada automotiva.
- **Descrição sugerida (revisar com o dono antes de publicar):**

> A EMDI Higienização cuida de sofás, colchões, cadeiras, poltronas e estofados automotivos na Grande São Paulo. Com produtos profissionais e extração profunda, a higienização vai além da superfície e remove sujeiras e resíduos acumulados nas fibras. Também fazemos impermeabilização, estética automotiva e lavagem detalhada automotiva. Solicite seu orçamento pelo WhatsApp (11) 94046-5840 e envie uma foto do seu estofado. Cuidar é mais que limpar, é transformar.

- **Fotos:** publicar os antes e depois reais, sempre com o mesmo ângulo nas duas fotos.
- **Rotina:** pedir avaliação a cada cliente satisfeito, enviando o link do perfil pelo WhatsApp logo após o serviço.

## 6. Pendências de conteúdo

- `privacidade.html`: preencher `[DATA DE PUBLICAÇÃO]` e `[CNPJ OU NOME DO RESPONSÁVEL]`.
- Depoimentos: colar avaliações reais do Google no espaço marcado em `index.html` (seção "Quem contratou, recomenda").
- Couro: incluir o serviço só após confirmação.

## 7. Teste final

Abrir o endereço publicado no Android e no iPhone e conferir: modelo 3D, passada do colchão, conversa guiada abrindo o WhatsApp, montador de orçamento e aviso de cookies.
