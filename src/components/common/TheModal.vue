<template>
  <b-modal
    id="C13"
    :modal-class="[$getTemplateID(), $getTemplateProcess(), modalClass]"
    header-class="justify-content-center text-center"
    content-class="content-class"
    :body-class="['body-class', { 'text-center': bodyCenter }]"
    footer-class="justify-content-center"
    :visible="true"
    centered
    scrollable
    hide-header-close
    :hide-header="hideHeader"
    :ok-only="okOnly"
    :title="$t(title)"
    :ok-title="$t(okTitle)"
    :cancel-title="$t(cancelTitle)"
    @hidden="$emit('hidden')"
    @cancel="$emit('cancel')"
    @ok="$emit('ok')"
    :hide-footer="hideButton"
  >
    <template #modal-header="{ close }">
      <span v-if="backBtn" class="back-btn material-icons" @click="$emit('back')">arrow_back </span>
      <h5 class="modal-title">{{ $t(title) }}</h5>
      <span v-if="closeBtn" class="close-btn material-icons" @click="close">close </span>
    </template>
    <slot></slot>
  </b-modal>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: "prompt",
    },
    okOnly: {
      type: Boolean,
      default: true,
    },
    backBtn: {
      type: Boolean,
      default: false,
    },
    closeBtn: {
      type: Boolean,
      default: true,
    },
    okTitle: {
      type: String,
      default: "confirm",
    },
    cancelTitle: {
      type: String,
      default: "cancel",
    },
    bodyCenter: {
      type: Boolean,
      default: true,
    },
    hideButton: {
      type: Boolean,
      default: false,
    },
    hideHeader: {
      type: Boolean,
      default: false,
    },
    modalClass: {
      type: String,
      default: "",
    },
  },
  data() {
    return {};
  },
  computed: {},
  methods: {},
};
</script>

<style lang="scss" scoped>
>>> #C13 {
  &.modal {
    top: 60px;
    height: calc(100% - 120px);
  }

  .content-class {
    border-radius: 10px;
    width: 85%;
  }

  .modal-header {
    border-bottom: 0;
    padding: 0.75rem;
  }

  .body-class {
    padding: 0.75rem;
  }

  .modal-title {
    font-size: 19px;
    font-weight: medium;
  }

  .modal-footer {
    border-top: 0;
    flex-wrap: nowrap;
    padding: 0.5rem;

    .btn {
      flex: 1;
      min-height: 43px;
      font-size: 19px;
      border-radius: 8px;
      border: 0;
    }
  }

  .back-btn,
  .close-btn {
    position: absolute;
    top: 10px;
    width: 30px;
    height: 30px;
    line-height: 30px;
    font-size: 20px;
    cursor: pointer;
  }

  .back-btn {
    left: 0;
  }

  .close-btn {
    right: 0;
  }

  &.C1311 {
    .content-class {
      background-color: #ffffff;
      color: #000000;
      border: solid 2px #00cafb;
    }

    .modal-title {
      color: #000000;
    }

    .btn-primary {
      $background: #00cafb;
      $color: #fff;
      $border: 1px solid #00cafb;

      background: $background;
      color: $color;
      border: $border;
      &:active {
        background: $background;
        color: $color;
        border: $border;
      }
    }

    .btn-secondary {
      $background: #efefef;
      $color: #000000;
      $border: 1px solid #efefef;

      background: $background;
      color: $color;
      border: $border;
      &:active {
        background: $background;
        color: $color;
        border: $border;
      }
    }
  }

  &.C1312 {
    .content-class {
      background-color: #ffffff;
      color: #000000;
    }

    .modal-title {
      color: #000000;
    }

    .btn-primary {
      $background: #c30001;
      $color: #fff;
      $border: 1px solid #c30001;

      background: $background;
      color: $color;
      border: $border;
      &:active {
        background: $background;
        color: $color;
        border: $border;
      }
    }

    .btn-secondary {
      $background: #4d4d4d;
      $color: #fff;
      $border: 1px solid #4d4d4d;

      background: $background;
      color: $color;
      border: $border;
      &:active {
        background: $background;
        color: $color;
        border: $border;
      }
    }

    &.marquee {
      .modal-content {
        border-color: #ff0000;
      }
    }
  }

  &.C1313 {
    .content-class {
      background-color: #ffffff;
      color: #000000;
      border: solid 2px #ffaa00;
    }

    .modal-title {
      color: #000000;
    }

    .btn-primary {
      $background: #ffaa00;
      $color: #fff;
      $border: 1px solid #ffaa00;

      background: $background;
      color: $color;
      border: $border;
      &:active {
        background: $background;
        color: $color;
        border: $border;
      }
    }

    .btn-secondary {
      $background: #efefef;
      $color: #000000;
      $border: 1px solid #efefef;

      background: $background;
      color: $color;
      border: $border;
      &:active {
        background: $background;
        color: $color;
        border: $border;
      }
    }
  }
}
</style>
