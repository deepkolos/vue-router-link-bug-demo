<style scoped>
.f-link {
  display: block;
}
</style>

<script>
export default {
  name: 'f-link',
  functional: true,

  props: {
    tag: String,
    to: {
      type: [String, Object],
      required: true
    },

    append: {
      type: Boolean,
      default: false
    },
    replace: {
      type: Boolean,
      default: false
    },

    context: Object
  },

  render(h, context) {
    const staticClass = context.data ? context.data.staticClass || '' : '';

    return h(
      'router-link',
      {
        props: context.props,
        attrs: {
          class: `f-link ${staticClass}`
        }
      },
      context.children
    );
  }
};
</script>
