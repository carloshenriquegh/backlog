#github/repo #obsidian/vault #obsidian/plugins/git #pkm
# Backup vault para repo remoto para github user owner: carloshenriquefnt

Repositorio [obsidian-vault-carlos7z](https://github.com/carlos7z/obsidian-vault-carlos7z) no [github-carlos7z](https://github.com/carlos7z). Após a criação do diretorio copiar a linha ssh do github:
	`git@github.com:carlos7z/backup-obsidian-carloz7z.git`

Sequencia de inicialização até o push dos arquivos para o github

```bash
git init
git remote add origin git@github.com:carlos7z/obsidian-vault-carlos7z.git
git add .
git commit -m 'initial commit'
git push --set-upstream origin master
```

Ao utilizar o push podem ocorrer problemas relacionados a:

1. Uso do git push `git push --set-upstream main` como 'main' pode não gerar resultado. Substituir `main` por `master`
2. Problema de [autenticação ssh](git-authsshkey.md)


# Backups alternativos
<a id="2. Backups Alternativos"></a>

1. Backup automático com plugin git do obsidian [community-plugins](/c/community-plugins.md).

2. Backup síncrono com app [syncthing](s/syncthing.md) (pc e mobile) (alternativo).
