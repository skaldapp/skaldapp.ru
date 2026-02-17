---
title: Main
description: Description
icon: twemoji:page-facing-up
attrs:
  un-cloak: true
---

# SKALD{.text-center}

::ul{#download.not-prose.flex-inline.flex-wrap.gap-8.justify-center.w-full.my-24.font-medium}

* [:span[]{.i-material-icon-theme-folder-public-open.size-11.align-middle} webapp](https://skaldapp.github.io/skaldapp)

* [:span[]{.i-material-icon-theme-folder-windows-open.size-11.align-middle} windows](https://github.com/skaldapp/skaldapp/releases/latest)

* [:span[]{.i-material-icon-theme-folder-macos-open.size-11.align-middle} macos](https://github.com/skaldapp/skaldapp/releases/latest)

* [:span[]{.i-material-icon-theme-folder-linux-open.size-11.align-middle} appimage](https://github.com/skaldapp/skaldapp/releases/latest)

* [:span[]{.i-material-icon-theme-folder-snapcraft-open.size-11.align-middle} snap](https://snapcraft.io/skaldapp)

::

![1.00](uploads/mountain.svg "Мощный редактор для писателей и разработчиков с кристально чистым интерфейсом"){#mountain.not-prose.mb-24}

## Мощный редактор для писателей и разработчиков с кристально чистым интерфейсом

**Skald** – это инновационный текстовый редактор с поддержкой **Markdown**, созданный для тех, кто ценит **простоту, гибкость и безопасность** 🛡️✨. Он идеально подходит как для **писателей**, так и для **разработчиков**, предлагая **чистый и интуитивно понятный интерфейс**, который помогает сосредоточиться на главном – **творчестве и продуктивности** 🚀📝.

## 🚀 Ваш личный помощник 🤖 Интеграция с искусственным интеллектом

* Skald может стать вашим **личным помощником** 🤖✨:

  * Генерация идей и креативного контента.

  * Редактирование и улучшение текстов.

  * Автоматическое создание контента по заданным параметрам.

![1.00](uploads/light.png){#light.my-24}

![1.00](uploads/dark.png){#dark.my-24}

## 🌟 Уровни функциональности 🌟 {.text-center}

::ul{#levels.not-prose.flex-inline.flex-wrap.gap-x-8.gap-y-24.justify-center.w-full.my-24.text-center}

* ![1.00](uploads/emerald.png){#emerald.drop-shadow-2xl.drop-shadow-emerald-500/20}

  :::elCard{.h-full.pt-18.max-w-sm shadow="hover"}

  #header

  **ПРОСТОЙ**{.text-[var(--nord14)]}

  ● {.text-[var(--nord14)]}

  #default

  * древовидные заметки с поддержкой **markdown**

  * визуальный редактор с **wysiwyg** режимом

  * идеально подходит для **заметок, статей, документации и книг**

  #footer

  :elButton[ПРОСТОЙ ПРИМЕР]{type="success" size="large" tag="RouterLink" to="/easy/"}

  :::

* ![1.00](uploads/ruby.png){#ruby.drop-shadow-2xl.drop-shadow-red-500/20}

  :::elCard{.h-full.pt-18.max-w-sm shadow="hover"}

  #header

  **ПРОДВИНУТЫЙ**{.text-[var(--nord11)]}

  ● {.text-[var(--nord11)]}

  #default

  * поддержка **html и tailwindcss** для создания стильных и современных страниц

  * **frontmatter** для управления метаданными и настройками страницы

  * ваши заметки превратятся в **красивый веб-ресурс** с удобной навигацией и адаптивным дизайном

  #footer

  :elButton[ПРОДВИНУТЫЙ ПРИМЕР]{type="danger" size="large" tag="RouterLink" to="/medium/"}

  :::

* ![1.00](uploads/diamond.png){#diamond.drop-shadow-2xl.drop-shadow-blue-500/20}

  :::elCard{.h-full.pt-18.max-w-sm shadow="hover"}

  #header

  **ПРОФЕССИОНАЛЬНЫЙ**{.text-[var(--nord10)]}

  ● {.text-[var(--nord10)]}

  #default

  * реактивность и управление динамическими данными с помощью **vue**

  * интеграция **сторонних библиотек** для расширения функциональности

  * разработка **сложных веб-приложений** прямо в редакторе

  #footer

  :elButton[ПРОФЕССИОНАЛЬНЫЙ ПРИМЕР]{type="primary" size="large" tag="RouterLink" to="/hard/"}

  :::

::

***

### 🚀 Готовы попробовать Skald?

Начните творить, создавать и развивать свои проекты **уже сегодня**! Skald – это ваш **надежный спутник** в мире текстов и веб-разработки 🌍💖.

<style scoped lang="postcss">
#levels {
  &>li {
    @apply relative;
  }

  & .el-card__body li {
    @apply my-6;
  }

  & img {
    @apply "absolute top-0 left-1/2 block w-32 -translate-x-1/2 -translate-y-1/2 hover:-translate-y-2/3 transition-transform duration-700";
  }

  & figcaption {
    @apply "text-center font-bold text-xl mb-4 uppercase after:content-['●'] after:block after:my-4";
  }
}

#download a {
  @apply "border-2 transition hover:text-[var(--nord10)] rounded-md p-4 hover:bg-[var(--nord5)] whitespace-nowrap";
}

#mountain {
  @apply "dark:invert";
}
</style>
