<div class="card-display">
  <div class="card-container">
    <Card style="min-width: 800px;" padded>
      <div class="card-contents">
        <img
          src="https://place-hold.it/190x190?text=square&fontsize=23"
          style="width: 190px;"
        />
        <div class="card-info" style="width: 590px; padding: 10px;">
          <h1>ABC123456_設備名A</h1>
          <Set chips={choices1} let:chip>
            <Chip {chip}>
              <Text>{chip}</Text>
            </Chip>
          </Set>
          <div style="display: flex; align-items: center;">
            <IconButton class="material-icons" style="color: red;">picture_as_pdf</IconButton>
            × 1
            <IconButton class="material-icons" style="color: blue;">description</IconButton>
            × 4
            <IconButton class="material-icons" style="color: green;">description</IconButton>
            × 1
          </div>
        </div>
      </div>
    </Card>
    <Card style="min-width: 800px;" padded>
      <div class="card-contents">
        <img
          src="https://place-hold.it/190x190?text=square&fontsize=23"
          style="width: 190px;"
        />
        <div class="card-info" style="width: 590px; padding: 10px;">
          <h1>DEF123456_設備名B</h1>
          <Set chips={choices2} let:chip>
            <Chip {chip}>
              <Text>{chip}</Text>
            </Chip>
          </Set>
          <div style="display: flex; align-items: center;">
            <IconButton class="material-icons" style="color: red;">picture_as_pdf</IconButton>
            × 2
            <IconButton class="material-icons" style="color: blue;">description</IconButton>
            × 1
            <IconButton class="material-icons" style="color: green;">description</IconButton>
            × 1
          </div>
        </div>
      </div>
    </Card>
    <Card style="min-width: 800px;" padded>
      <div class="card-contents">
        <img
          src="https://place-hold.it/190x190?text=square&fontsize=23"
          style="width: 190px;"
        />
        <div class="card-info" style="width: 590px; padding: 10px;">
          <h1>GHI123456_設備名C</h1>
          <Set chips={choices3} let:chip>
            <Chip {chip}>
              <Text>{chip}</Text>
            </Chip>
          </Set>
          <div style="display: flex; align-items: center;">
            <IconButton class="material-icons" style="color: red;">picture_as_pdf</IconButton>
            × 1
            <IconButton class="material-icons" style="color: blue;">description</IconButton>
            × 2
            <IconButton class="material-icons" style="color: green;">description</IconButton>
            × 2
          </div>
        </div>
      </div>
    </Card>
    <Card style="min-width: 800px;" padded>
      <div class="card-contents">
        <img
          src="https://place-hold.it/190x190?text=square&fontsize=23"
          style="width: 190px;"
        />
        <div class="card-info" style="width: 590px; padding: 10px;">
          <h1>JKL123456_設備名D</h1>
          <Set chips={choices4} let:chip>
            <Chip {chip}>
              <Text>{chip}</Text>
            </Chip>
          </Set>
          <div style="display: flex; align-items: center;">
            <IconButton class="material-icons" style="color: red;">picture_as_pdf</IconButton>
            × 1
            <IconButton class="material-icons" style="color: blue;">description</IconButton>
            × 2
            <IconButton class="material-icons" style="color: green;">description</IconButton>
            × 2
          </div>
        </div>
      </div>
    </Card>
  </div>
</div>

<script lang="ts">
  import Card, {
    Content,
    Media,
  } from '@smui/card';
  import Chip, { Set, Text } from '@smui/chips';
  import IconButton from '@smui/icon-button';

  let choices1 = ['担当者A', '納品先A', '商社A'];
  let choices2 = ['担当者B', '納品先B'];
  let choices3 = ['担当者A', '納品先C'];
  let choices4 = ['担当者B', '納品先D', '商社B'];
</script>

<style>
  .card-container {
    display: flex;
    flex-direction: column;
    gap: 10px 0;
  }

  .card-contents {
    display: flex;
  }

  .card-info h1 {
    margin: 10px;
  }
</style>
