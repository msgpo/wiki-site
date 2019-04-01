<template lang='pug'>
  v-footer.footer(height='auto')
    v-container.pa-0(fluid, grid-list-xl)
      v-container
        v-layout(row, wrap)
          v-flex.footer-col(xs12, md12, lg3)
            img.footer-logo(:src='require("../assets/logos/requarks.svg")')
            .mt-4 Open source applications for teams
          v-flex.footer-col(xs12, sm4, lg3)
            .footer-subtitle Documentation
            ul.footer-links
              li: a(href='https://docs-beta.requarks.io/install/requirements') Requirements
              li: a(href='https://docs-beta.requarks.io/install') Install
              li: a(href='https://docs-beta.requarks.io/install/upgrade') Upgrade
              li: a(href='https://docs-beta.requarks.io/') More topics...
          v-flex.footer-col(xs12, sm4, lg3)
            .footer-subtitle Contribute
            ul.footer-links
              li: a(href='https://www.patreon.com/requarks') Donate on Patreon
              li: a(href='https://opencollective.com/wikijs') Donate on OpenCollective
              li: a(href='https://docs-beta.requarks.io/dev/translations') Help with Translations
              li: a(href='https://requests.requarks.io/wiki') Request a New Feature
              li: a(href='https://github.com/Requarks/wiki/issues') Report a Bug
              li: a(href='https://docs-beta.requarks.io/dev') Developers
          v-flex.footer-col(xs12, sm4, lg3)
            .footer-subtitle About
            ul.footer-links
              li: a(href='https://github.com/Requarks/wiki') GitHub Project
              li: a(href='https://twitter.com/requarks') Follow on Twitter
              li: a(href='https://gitter.im/Requarks/wiki') Chat on Gitter
              li: a(href='/about') Contributors &amp; Sponsors
      v-divider.mt-5
      v-container.footer-bar
        v-layout(row, wrap, align-center)
          v-flex(xs12, md4)
            div Released under the #[strong AGPL-v3 License]
            div Copyright © 2017-{{currentYear}} #[a(href='https://www.requarks.io/', title='requarks.io') Requarks.io]
          v-flex.hidden-sm-and-down.text-xs-center(md4)
            a.mr-4(href='https://github.com/Requarks/wiki', title='GitHub Project'): img(:src='require("../assets/logos/metro-github.svg")', alt='GitHub')
            a(href='https://twitter.com/requarks', title='Twitter'): img(:src='require("../assets/logos/metro-twitter.svg")', alt='Twitter')
          v-flex(xs12, md4)
            a(href='https://status.requarks.io/', title='Service Status') Service Status
</template>

<script>
export default {
  name: 'SiteFooter',
  data () {
    return {
      currentYear: new Date().getFullYear()
    }
  }
}
</script>

<style lang='scss'>
.theme--light.v-footer.footer {
  background-color: var(--v-greyish-base);
  background-image: url('../assets/shapes/shape1.svg');
  background-repeat: no-repeat;
  background-size: 100%;
  background-position: 40vw 120px;
}

.footer {
  padding-top: 75px;
  font-weight: 300;

  @media screen and (max-width: 599px) {
    padding-top: 30px;
  }

  &-logo {
    width: 100%;
    max-width: 270px;
  }
  &-subtitle {
    font-weight: 600;
    font-size: 18px;
  }
  &-links {
    list-style-type: none;
    padding: 0;

    li {
      display: block;
      margin: 16px 0;

      @media screen and (max-width: 599px) {
        margin: 8px 0;
      }

      a {
        color: var(--v-greyish-darken1);
        text-decoration: none;
        font-size: 16px;
        transition: color .4s linear;

        &:hover {
          color: var(--v-primary-base);
        }
      }
    }
  }
  &-col {
    @media screen and (max-width: 1264px) {
      text-align: center;
    }
  }
  &-bar {
    color: var(--v-greyish-darken1);

    @media screen and (max-width: 1264px) {
      text-align: center;
    }

    a {
      color: var(--v-greyish-darken1);
      text-decoration: none;
      transition: color .4s linear;

      &:hover {
        color: var(--v-primary-base);
      }
    }

    .flex:last-child {
      text-align: right;

      @media screen and (max-width: 1264px) {
        text-align: center;
      }
    }
  }
}
</style>