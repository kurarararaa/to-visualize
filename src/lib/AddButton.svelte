<div class="flexy">
  <div class="margins">
    <Fab color="primary" on:click={() => (open = true)}>
      <Icon class="material-icons">add</Icon>
    </Fab>
  </div>
</div>

<Dialog
  bind:open
  fullscreen
  aria-labelledby="over-fullscreen-title"
  aria-describedby="over-fullscreen-content"
>
  <Header>
    <Title id="over-fullscreen-title">完成図書登録</Title>
    <IconButton action="close" class="material-icons">close</IconButton>
  </Header>
  <Content id="over-fullscreen-content">
    <div class="entry-container">
      <Textfield style="width: 200px;" bind:value={valueA} label="工事番号"></Textfield>
      <Textfield style="width: 500px;" bind:value={valueB} label="設備名"></Textfield>
      <Textfield
        style="width: 100%; margin-top: 20px;"
        helperLine$style="width: 100%;"
        textarea
        bind:value={valueC}
        label="Memo"
      >
      </Textfield>
      <pre class="status">タグ：</pre>
      <Set chips={choices} let:chip>
        <Chip {chip}>
          <Text>{chip}</Text>
        </Chip>
      </Set>
      <pre class="status">添付ファイル：</pre>
      <div style="display: flex; align-items: center;">
        <IconButton class="material-icons" style="color: red;">picture_as_pdf</IconButton>
        <a>202206021947230000.pdf</a>
        <Set chips={choices2} let:chip>
          <Chip style="margin-left: 20px;" {chip}>
            <Text>{chip}</Text>
          </Chip>
        </Set>
      </div>
      <div style="display: flex; align-items: center;">
        <IconButton class="material-icons" style="color: blue;">description</IconButton>
        <a>202206021947230000.docx</a>
        <Set chips={choices2} let:chip>
          <Chip style="margin-left: 20px;" {chip}>
            <Text>{chip}</Text>
          </Chip>
        </Set>
      </div>
    </div>
  </Content>
  <Actions>
    <Button action="reject">
      <Label>削除</Label>
    </Button>
    <Button action="accept" defaultAction>
      <Label>保存</Label>
    </Button>
  </Actions>
</Dialog>

<script lang="ts">
  import Fab, { Icon } from '@smui/fab';
  import Textfield from '@smui/textfield';
  import Dialog, {
    Header,
    Title,
    Content,
    Actions,
    InitialFocus,
  } from '@smui/dialog';
  import IconButton from '@smui/icon-button';
  import Button, { Label } from '@smui/button';
  import Chip, { Set, Text } from '@smui/chips';

  let open = false;
  let subOpen = false;
  let selection = 'Radishes';
  let selected = 'Nothing yet.';
  let response = 'Nothing yet.';

  let valueA = null;
  let valueB = null;
  let valueC = '';

  let choices = ['担当者A', '納品先A', '商社A', '+'];
  let choices2 = ['x'];
</script>

<style>
	.flexy {
		position: fixed;
    bottom: 10vh;
    right: 10vw;
	}

  .entry-container {
    display: flex;
    flex-direction: column;
    padding: 30px;
    min-height: 350px;
  }
</style>
