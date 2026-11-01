# Windows Dock — beta para testers

Uma dock inspirada no macOS para Windows 10/11: ícones com magnificação, apps abertos, e um modo
"Smart" com sistema, clima, mídia, atalhos e jogos. Ela não substitui o Explorer e não precisa de
administrador.

> Este repositório só distribui os instaladores de teste. O código-fonte não é público.

## Instalar

1. Vá em **[Releases](../../releases/latest)** e baixe o `WindowsDock_x.y.z_x64-setup.exe`.
2. Execute. O Windows pode mostrar **"O Windows protegeu o computador"** porque o instalador ainda
   não é assinado: clique em **Mais informações → Executar assim mesmo**.
3. A Dock aparece na parte de baixo da tela, e um ícone fica na bandeja (perto do relógio).

Instala só para o seu usuário, em `%LOCALAPPDATA%\Windows Dock`.

## Atualizações

A Dock verifica sozinha se existe uma versão nova alguns segundos depois de abrir e pergunta se você
quer atualizar. Também dá para forçar: **ícone na bandeja → Verificar atualizações…**

## Se algo der errado com a barra de tarefas

A Dock pode esconder a barra de tarefas do Windows (opção nas configurações). Ela sempre pode voltar:

- Atalho **Ctrl + Alt + Shift + R** (de qualquer lugar), ou
- **ícone na bandeja → Restaurar barra de tarefas do Windows**, ou
- simplesmente **sair da Dock** (bandeja → Sair) — a barra volta como estava.

Se a Dock travar, a barra é devolvida automaticamente. Em último caso, abra o Executar (**Win + R**) e
rode:

```
"%LOCALAPPDATA%\Windows Dock\windows-dock.exe" --restore-taskbar
```

Para abrir a Dock sem mexer na barra de tarefas: `windows-dock.exe --safe-mode`.

## Reportar bug ou ideia

Abra uma **[Issue](../../issues/new/choose)** — precisa de uma conta no GitHub (é grátis).
Para bugs, anexe o log mais recente, que fica em:

```
%LOCALAPPDATA%\com.saru.windowsdock\logs
```

(cole esse caminho na barra de endereço do Explorer). Prints ou um vídeo curto ajudam muito.

## Desinstalar

**Configurações do Windows → Aplicativos → Windows Dock → Desinstalar.** A barra de tarefas volta ao
estado original. As preferências ficam em `%APPDATA%\com.saru.windowsdock` — apague a pasta para zerar.
