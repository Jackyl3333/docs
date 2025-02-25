---
title: Fazer merge automático de um pull request
intro: Você pode aumentar a velocidade de desenvolvimento permitindo o merge automático de um pull request para que o pull request seja mesclado automaticamente quando todos os requisitos de merge forem atendidos.
product: '{% data reusables.gated-features.auto-merge %}'
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Pull requests
redirect_from:
  - /github/collaborating-with-issues-and-pull-requests/incorporating-changes-from-a-pull-request/automatically-merging-a-pull-request
  - /github/collaborating-with-issues-and-pull-requests/automatically-merging-a-pull-request
  - /github/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/automatically-merging-a-pull-request
shortTitle: Fazer merge do PR automaticamente
---

## Sobre o merge automático

If you enable auto-merge for a pull request, the pull request will merge automatically when all required reviews are met and all required status checks have passed. O merge automático impede que você espere que os sejam atendidos para que você possa passar para outras tarefas.

Antes de usar o merge automático com um pull request, o merge automático deve ser habilitado para o repositório. Para obter mais informações, consulte "[Gerenciar merge automático para pull requests no seu repositório](/github/administering-a-repository/managing-auto-merge-for-pull-requests-in-your-repository).

Depois que você ativar o merge automático para uma pull request, se alguém que não tiver permissões de gravação no repositório fizer push de novas alterações no branch principal ou alterar o branch de base do pull request, o merge automático será desabilitado. Por exemplo, se um mantenedor permitir o merge automático para um pull request a partir de uma bifurcação, o merge automático será desabilitado depois que um colaborador fizer push de novas alterações no pull request.

Você pode fornecer feedback sobre a o merge automático por meio de uma discussão [{% data variables.product.prodname_github_community %}](https://github.com/orgs/community/discussions/categories/pull-requests).

## Habilitar merge automático

{% data reusables.pull_requests.auto-merge-requires-branch-protection %}

Pessoas com permissões de gravação em um repositório podem habilitar o merge automático em um pull request.

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-pr %}
1. Na lista "Pull Requests", clique no pull request para o qual você deseja fazer o merge automático.
1. Opcionalmente, para escolher um método de merge, selecione o menu suspenso **Habilitar merge automático** e, em seguida, clique em um método de merge. Para obter mais informações, consulte "[Sobre merges da pull request](/github/collaborating-with-issues-and-pull-requests/about-pull-request-merges)". ![Menu suspenso "Habilitar merge automático"](/assets/images/help/pull_requests/enable-auto-merge-drop-down.png)
1. Clique **Habilitar merge automático**. ![Botão para habilitar merge automático](/assets/images/help/pull_requests/enable-auto-merge-button.png)
  {% ifversion fpt %}
1. Se você escolheu os métodos de merge ou combinação por squash, digite uma mensagem de commit e a descrição e escolha o endereço de e-mail que você deseja criar o commimt de merge.![Campos para inserir mensagem de commit e descrição e escolher o e-mail do autor do commit](/assets/images/help/pull_requests/pull-request-information-fields.png)
  {% note %}

  **Observação:** O menu suspenso de e-mail não está disponível se você tiver a privacidade do e-mail habilitada ou se você tiver apenas um e-mail verificado e visível associado à sua conta do {% data variables.product.company_short %}.

  {% endnote %}
  {% endif %}
  {% ifversion ghes or ghae or ghec %}
1. Se você escolheu os métodos de merge ou combinação por squash e merge, digite uma mensagem de commit e descrição. ![Campos para inserir a mensagem e a descrição do commit](/assets/images/help/pull_requests/pull-request-information-fields-enterprise.png)
  {% endif %}
1. Clique em **Confirmar merge automático**.

## Desabilitar o merge automático

As pessoas com permissões de gravação em um repositório e autores de pull request podem desabilitar o merge automático em um pull request.

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-pr %}
1. Na lista "Pull Requests", clique no pull request para o qual você deseja desabilitar o merge automático.
1. Na caixa de merge, clique em **Desabilitar o merge automático**. ![Botão para desabilitar o merge automático](/assets/images/help/pull_requests/disable-auto-merge-button.png)
