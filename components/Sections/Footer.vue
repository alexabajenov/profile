<template>
  <footer :class="$style.footer">
    <div :class="$style.container">
      <div :class="$style.header">
        <h2>Contact <span>me</span></h2>
        <div :class="$style.imageContainer">
          <img src="~/assets/img/cuate.png" alt="cuate">
        </div>
      </div>
      <div :class="$style.emailComtainer">
        <h3>Say Hello!</h3>
        <a href="mailto:alexandra.bajenova1@gmail.com">alexandra.bajenova1@gmail.com</a>
      </div>
      <div :class="$style.footerInfo">
        <div :class="$style.infoItem">
          <ul>
            <li>Let’s talk</li>
            <li>
              <span :class="$style.icon">
                <img src="~assets/img/email.svg" alt="email">
              </span>
              <a href="mailto:alexandra.bajenova1@gmail.com">alexandra.bajenova1@gmail.com</a></li>
            <li>
              <span :class="$style.icon">
                <img src="~assets/img/instagram.svg" alt="email">
              </span>
              alexandrabajenova16
            </li>
            <li>
              <span :class="$style.icon">
                <img src="~assets/img/phone.svg" alt="email">
              </span>
              <a href="tel:+37379944924">+37379944924</a>
            </li>
            <li>
              <span :class="$style.icon">
                <img src="~assets/img/vk.svg" alt="email">
              </span>
              sashenika13
            </li>
          </ul>
        </div>
        <div :class="$style.infoItem">
          <ul>
            <li>Info</li>
            <li>designed by Alexandra Bajenova</li>
          </ul>
        </div>
        <div :class="$style.infoItem">
          <ul>
            <li>Why me?</li>
            <li>you should choose me because I am a very responsible and competent person in my work!</li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default ({
  //
})
</script>

<style module lang="scss">
.footer {
  width: 100%;
  .container {
    width: 100%;
    max-width: var(--max-content-width);
    margin: 0 auto;
    padding: 50px var(--content-horizontal-spacing) 32px var(--content-horizontal-spacing);
    background-color: var(--layout-color-1);
    display: flex;
    flex-direction: column;
    align-items: center;
    .header {
      display: flex;
      justify-content: space-between;
      width: 100%;
      > h2 {
        font-size: var(--text-xl);
        white-space: nowrap;
        span {
          color: var(--second-text-color);
        }
      }
      .imageContainer {
        display: flex;
        > img {
          width: 100%;
          height: auto;
        }
      }
    }
    .emailComtainer {
      width: 100%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: var(--spacing-4xl) var(--spacing-xl);
      border-radius: var(--border-radius-2);
      background-color: var(--layout-color-2);
      margin-bottom: 117px;
      color: var(--white);
      h3 {
        font-size: var(--text-xl);
        font-weight: 400;
      }
      > a {
        color: var(--white);
        transition: 0.3s;
          &:hover {
          color: var(--second-text-color);
        }
      }
    }
    .footerInfo {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      justify-content: center;
      gap: var(--spacing-m);
      width: 100%;
      .infoItem {
        width: 100%;
        ul {
          li:first-child {
            font-family: 'Montserrat Alternates';
            font-size: var(--text-l);
            color: var(--second-text-color);
            margin-bottom: var(--spacing-l);
          }
          li:not(:first-child) {
            display: flex;
            align-items: center;
            font-size: var(--text-s);
            margin-bottom: var(--spacing-xs);
            
            .icon {
              display: inline-block;
              width: 24px;
              height: auto;
              margin-right: var(--spacing-m);
              img {
                width: 100%;
                height: auto;
              }
            }
            > a {
              transition: 0.3s;
              &:hover {
                color: var(--second-text-color);
              }
            }
          }
        } 
      }
    }
  }
}
</style>