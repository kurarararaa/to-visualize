<div class="margins search-area">
  <Textfield
    class="shaped-outlined"
    variant="outlined"
    bind:value
    label="#タグやキーワードで検索"
    style="min-width: 500px;"
  >
  </Textfield>
</div>

<script>
  import Textfield from '@smui/textfield';

  let value = null;
</script>

<style>
  .search-area {
    min-height: 15vh;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
  }

  *
    :global(.shaped-outlined
      .mdc-notched-outline
      .mdc-notched-outline__leading) {
    border-radius: 28px 0 0 28px;
    width: 28px;
  }
  *
    :global(.shaped-outlined
      .mdc-notched-outline
      .mdc-notched-outline__trailing) {
    border-radius: 0 28px 28px 0;
  }
  * :global(.shaped-outlined .mdc-notched-outline .mdc-notched-outline__notch) {
    max-width: calc(100% - 28px * 2);
  }
  *
    :global(.shaped-outlined.mdc-text-field--with-leading-icon:not(.mdc-text-field--label-floating)
      .mdc-floating-label) {
    left: 16px;
  }
  * :global(.shaped-outlined + .mdc-text-field-helper-line) {
    padding-left: 32px;
    padding-right: 28px;
  }
</style>
