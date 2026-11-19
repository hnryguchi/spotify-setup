# Meu Spotify com Spicetify

**Português** · [English](README.en.md)

O Spotify que eu uso no computador: tema translúcido, letras ao vivo e fundo que muda com a capa do álbum.
Tudo instalado pelo **Spicetify**, sem mexer em código. Leva uns 5 minutos.

**Me segue lá:** [open.spotify.com/user/31ilerrhi3kodpoigqprs65xdrz4](https://open.spotify.com/user/31ilerrhi3kodpoigqprs65xdrz4)

## O que tem no meu setup

| Tipo | Nome | O que faz |
|---|---|---|
| Tema | [Hazy](https://github.com/Astromations/Hazy) | visual translúcido, com a capa do álbum desfocada no fundo |
| Extensão | [Beautiful Lyrics](https://github.com/surfbryce/beautiful-lyrics) | letras sincronizadas palavra por palavra, com fundo dinâmico |
| Extensão | [Spicy Lyrics](https://github.com/Spikerko/spicy-lyrics) | outra tela de letras ao vivo, em tela cheia |
| Extensão | [SpicyThemes](https://github.com/7xeh/SpicyThemes) | temas para a tela do Spicy Lyrics |

## Passo a passo (Windows)

**1. Instale o Spotify do site oficial**, não da Microsoft Store: [spotify.com/download](https://www.spotify.com/download/).
A versão da Store não funciona com o Spicetify. Abra o Spotify uma vez, faça login e feche.

**2. Instale o Spicetify.** Abra o **PowerShell** (menu Iniciar → digite "PowerShell") e cole:

```powershell
iwr -useb https://raw.githubusercontent.com/spicetify/cli/main/install.ps1 | iex
```

Quando ele perguntar *"Do you also want to install Spicetify Marketplace?"*, aperte **Enter** (sim).

**3. Abra o Spotify.** Vai aparecer uma aba nova, **Marketplace**, no menu do Spotify.

**4. Instale o tema e as extensões pelo Marketplace:**
- aba **Themes** → procure **Hazy** → **Install**;
- aba **Extensions** → procure e instale **Beautiful Lyrics**, **Spicy Lyrics** e **SpicyThemes**.

Pronto. Toque uma música e abra a letra (ícone de microfone) para ver as letras ao vivo.

<details>
<summary><b>macOS / Linux</b></summary>

No Terminal:

```bash
curl -fsSL https://raw.githubusercontent.com/spicetify/cli/main/install.sh | sh
```

Depois siga a partir do passo 3. No Linux, o Spotify instalado por Snap não funciona; use o pacote `.deb`/`.rpm` ou o Flatpak (veja a [documentação](https://spicetify.app/docs/advanced-usage/installation)).
</details>

## Se o Spotify atualizar e o visual sumir

Atualizações do Spotify desfazem o Spicetify. No PowerShell:

```powershell
spicetify update
spicetify backup apply
```

Se der erro, `spicetify restore backup apply` costuma resolver.

## Para voltar ao Spotify normal

```powershell
spicetify restore
```

## Bom saber

- O Spicetify **não é oficial** do Spotify. Ele modifica só o aplicativo no seu computador; a conta e as playlists não mudam.
- Os temas e as extensões são feitos por outras pessoas (links na tabela acima). Os créditos são delas.
- Documentação oficial: [spicetify.app](https://spicetify.app).
