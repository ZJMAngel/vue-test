<script>
import ElementCommonComp from './ElementCommonComp.vue';

export default {
  name: 'ElementComp',
  components: { ElementCommonComp },
  data() {
    return {
      input: '',
    };
  },
  render() {
    const type = 'button';

    return (
      <div>
        <ElementCommonComp type={type} plain onClick={() => console.log(1)}>
          555
        </ElementCommonComp>
        <ElementCommonComp
          type="input"
          v-model={this.input}
          onClick={() => console.log(1)}
        ></ElementCommonComp>
        <ElementCommonComp
          type="tag"
          v-model={this.input}
          onClick={() => console.log(2)}
          closable
          onClose={() => console.log(3)}
          size="mini"
        >
          {this.input}
        </ElementCommonComp>
      </div>
    );
  },
};
</script>
