<script>
import { Line, mixins } from 'vue-chartjs';

export const labels = [
  'January',
  'February',
  'March',
  'April',
  'May',
  'June',
  'July',
  'August',
  'September',
  'October',
  'November',
  'December',
];

// the chart may have issues with lifecycle
// when I stayed long on the page or I made changes to the code, the chart content disappear
export default {
  name: 'Chart',
  extends: Line,
  mixins: [mixins.reactiveProp],
  props: ['react', 'vue', 'angular'],
  mounted() {
    this.renderChart({
      labels,
      datasets: [
        {
          label: 'react downloads',
          backgroundColor: '#00d8ff',
          fill: false,
          data: this.react,
        },
        {
          label: 'vue downloads',
          backgroundColor: '#42b883',
          fill: false,
          data: this.vue,
        },
        {
          label: 'angular downloads',
          backgroundColor: '#ffd400',
          fill: false,
          data: this.angular,
        },
      ],
    });
  },
};
</script>

