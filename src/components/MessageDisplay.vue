<script>
import { getMessage } from "@/services/axios";

export default {
  data() {
    return {
      message: {},
      error: null,
    };
  },
  async created() {
    try {
      this.message = await getMessage();
    } catch (err) {
      this.error = "Oops! Something went wrong.";
    }
  },
};
</script>
