<template>
  <div>
    <div class="layout-padding">
      <p class="caption">Checkboxes</p>
      <div class="list">
        <label class="item">
          <div class="item-primary">
            <q-checkbox v-model="checked"></q-checkbox>
          </div>
          <div class="item-content">
            Notifications
          </div>
        </label>
        <label class="item two-lines">
          <div class="item-primary">
            <q-checkbox v-model="checked"></q-checkbox>
          </div>
          <div class="item-content">
            <div>Notifications</div>
            <div>Allow notifications</div>
          </div>
        </label>
        <label class="item three-lines">
          <div class="item-primary">
            <q-checkbox v-model="checked"></q-checkbox>
          </div>
          <div class="item-content">
            <div>Notifications</div>
            <div>Allow notifications Allow notifications Allow notifications Allow notifications Allow notifications </div>
          </div>
        </label>
      </div>

      <p class="caption">Radios</p>
      <div class="list">
        <label class="item">
          <div class="item-primary">
            <q-radio v-model="option" val="opt1"></q-radio>
          </div>
          <div class="item-content">
            Option 1
          </div>
        </label>
        <label class="item two-lines">
          <div class="item-primary">
            <q-radio v-model="option" val="opt2"></q-radio>
          </div>
          <div class="item-content">
            <div>Option 2</div>
            <div>Allows notifications</div>
          </div>
        </label>
        <label class="item three-lines">
          <div class="item-primary">
            <q-radio v-model="option" val="opt3"></q-radio>
          </div>
          <div class="item-content">
            <div>Option 3</div>
            <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</div>
          </div>
        </label>
      </div>

      <p class="caption">Toggles</p>
      <div class="list">
        <label class="item">
          <div class="item-content has-secondary">
            Events and reminders
          </div>
          <div class="item-secondary">
            <q-toggle v-model="checked"></q-toggle>
          </div>
        </label>
        <label class="item two-lines">
          <div class="item-content has-secondary">
            <div>Events and reminders</div>
            <div>Lorem ipsum</div>
          </div>
          <div class="item-secondary">
            <q-toggle v-model="checked" class="purple"></q-toggle>
          </div>
        </label>
        <label class="item three-lines">
          <div class="item-content has-secondary">
            <div>Events and reminders</div>
            <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</div>
          </div>
          <div class="item-secondary">
            <q-toggle v-model="checked" class="red"></q-toggle>
          </div>
        </label>
      </div>

      <p class="caption">Select</p>
      <div class="list">
        <div class="list-label">Single Selection</div>
        <div class="item two-lines">
          <i class="item-primary">supervisor_account</i>
          <div class="item-content">
            <q-select class="full-width" type="radio" v-model="select" :options="selectOptions" ok-label="Pick" cancel-label="Neah" title="Company"></q-select>
          </div>
        </div>
        <hr>
        <div class="list-label">Multiple Selection</div>
        <div class="item two-lines">
          <i class="item-primary">supervisor_account</i>
          <div class="item-content">
            <q-select class="full-width" type="checkbox" v-model="multipleSelect" :options="selectOptions" ok-label="Pick" title="Companies"></q-select>
          </div>
        </div>
        <div class="item two-lines">
          <i class="item-primary">supervisor_account</i>
          <div class="item-content">
            <q-select class="full-width" type="toggle" v-model="multipleSelect" :options="selectOptions" ok-label="Pick" title="Companies"></q-select>
          </div>
        </div>
      </div>

      <p class="caption">Ranges</p>
      <div class="list">
        <div class="item two-lines">
          <i class="item-primary">volume_up</i>
          <div class="item-content">
            <q-range v-model="range" :min="0" :max="50" label></q-range>
          </div>
        </div>
        <div class="item two-lines">
          <i class="item-primary">brightness_medium</i>
          <div class="item-content">
            <q-range v-model="range" :min="0" :max="50" label></q-range>
          </div>
        </div>
        <hr>
        <div class="list-label">Double Range</div>
        <div class="item two-lines">
          <i class="item-primary">local_atm</i>
          <div class="item-content">
            <q-double-range v-model="doubleRange" :min="0" :max="50" label></q-double-range>
          </div>
        </div>
        <div class="item two-lines">
          <i class="item-primary">euro_symbol</i>
          <div class="item-content">
            <q-double-range v-model="doubleRange" :min="0" :max="50" label></q-double-range>
          </div>
        </div>
      </div>

      <p class="caption">Date and Time</p>
      <div class="list">
        <div class="list-label">Date or Time</div>
        <div class="item two-lines">
          <i class="item-primary">access_time</i>
          <div class="item-content">
            <q-datetime class="full-width" v-model="timestamp" type="time"></q-datetime>
          </div>
        </div>
        <div class="item two-lines">
          <i class="item-primary">update</i>
          <div class="item-content row items-baseline">
            <q-datetime class="full-width" v-model="timestamp" type="date"></q-datetime>
          </div>
        </div>
        <hr>
        <div class="list-label">Date & Time</div>
        <div class="item two-lines">
          <i class="item-primary">notifications</i>
          <div class="item-content row items-baseline">
            <q-datetime class="full-width" v-model="timestamp" type="datetime"></q-datetime>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      checked: false,
      option: 'opt1',
      select: 'fb',
      multipleSelect: ['goog', 'twtr'],
      selectOptions: [
        {
          label: 'Google',
          value: 'goog'
        },
        {
          label: 'Facebook',
          value: 'fb'
        },
        {
          label: 'Twitter',
          value: 'twtr'
        },
        {
          label: 'Apple Inc.',
          value: 'appl'
        },
        {
          label: 'Oracle',
          value: 'ora'
        }
      ],
      range: 20,
      doubleRange: {
        min: 10,
        max: 35
      },
      timestamp: '2016-09-18T10:45:00.000Z'
    }
  }
}
</script>
