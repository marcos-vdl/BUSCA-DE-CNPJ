# 🏢 Consulta CNPJ & Busca Inteligente de Endereço

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/Licensa-MIT-green?style=for-the-badge)

Uma aplicação web de alta performance desenvolvida em **Vanilla JavaScript (100% nativo, sem frameworks)** para consulta completa de dados cadastrais de empresas (CNPJ) e busca híbrida e geolocalizada de endereços, CEPs e estabelecimentos comerciais no Brasil.

---

## 🌟 Pontos Fortes e Diferenciais Técnicos

* ⚡ **Zero Dependências (100% Native Web):** Aplicação extremamente leve, rápida e otimizada. Carregamento instantâneo sem necessidade de bundlers, React ou bibliotecas externas.
* 🔎 **Busca Híbrida de CNPJ & Razão Social:**
  * Auto-complete inteligente enquanto você digita a Razão Social ou Nome Fantasia.
  * Mascaramento automático e dinâmico do CNPJ (`00.000.000/0000-00`).
* 📊 **Dossiê Empresarial Completo:**
  * **Informações Gerais:** Razão Social, Nome Fantasia, Situação Cadastral, Data de Abertura e Regime Tributário (Simples Nacional).
  * **Inscrição Estadual (IE):** Busca assíncrona paralela em tempo real (não bloqueia o carregamento dos dados principais do CNPJ).
  * **Quadro de Sócios e Administradores (QSA):** Lista detalhada de sócios, suas qualificações, faixa etária e telefones associados.
  * **Atividades Econômicas:** CNAE Principal e CNAEs Secundários formatados.
* 📍 **Sistema Multicamadas de Busca de Local e Endereço:**
  * **Camada IBGE:** Filtro dinâmico de municípios sincronizado com o Estado (UF) selecionado.
  * **Camada BrasilAPI:** Resolução precisa de CEP v2.
  * **Camada OpenStreetMap (Nominatim):** Geocodificação de logradouros, bairros e estabelecimentos no mapa.
  * **Camada CNPJ Fallback:** Identificação de comércios locais por CNPJ quando não geolocalizados no mapa tradicional.
  * **Camada Google Maps:** Redirecionamento e geração de link direto para rotas e navegação.
* 💡 **UX/UI Interativa & Cruzamento de Dados:**
  * **Navegação Fluida por Modais:** Exibição clara e organizada dos dados sem poluir a interface.
  * **Conectividade entre Modais:** Ao clicar no endereço exibido no modal do CNPJ, o sistema abre automaticamente a visualização do local no mapa.
  * **Otimização de Requisições (Debounce):** Controle de tempo nos campos de busca para evitar requisições desnecessárias às APIs e prevenir *rate limiting*.

---

## 🛠️ Tecnologias Utilizadas

* **Frontend:** HTML5 Semântico, CSS3 Moderno (CSS Grid & Flexbox, Modais Responsivos).
* **Lógica:** JavaScript ES6+ (`async/await`, `Fetch API`, `Debounce Pattern`, manipulação dinâmica do DOM).
* **APIs Integradas:**
  * [BrasilAPI](https://brasilapi.com.br/) (Dados de CNPJ e CEP v2)
  * [CNPJ.ws](https://cnpj.ws/) (Auto-complete de empresas e Inscrição Estadual)
  * [IBGE Localidades](https://servicodados.ibge.gov.br/) (Municípios atualizados por UF)
  * [OpenStreetMap / Nominatim](https://nominatim.openstreetmap.org/) (Geocodificação e busca por locais)
  * [Google Maps Search API](https://www.google.com/maps) (Link direto para navegação)

---

## 🚀 Como Executar o Projeto

Como o projeto foi construído utilizando tecnologias nativas da web, não é necessário instalar dependências com `npm` ou `yarn`.

1. Clone o repositório:
   ```bash
   git clone https://github.com/MARCOS-VDL/BUSCA-DE-CNPJ.git
   ```
2. Navegue até a pasta do projeto:
   ```bash
   cd BUSCA-DE-CNPJ
   ```
3. Abra o arquivo `index.html` em qualquer navegador web de sua preferência.

---

## 📄 Licença

Este projeto está sob a licença MIT. Sinta-se à vontade para utilizar, estudar e aprimorar o código.
