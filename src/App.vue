<template>
	<div>
		<canvas ref="myChart" style="width: 100vw; height: 500px"></canvas>
	</div>
</template>

<script>
import Chart from "chart.js/auto";
export default {
	mounted() {
		const ctx = this.$refs.myChart.getContext("2d");
		const myChart = new Chart(ctx, {
			type: "bar",
			data: {
				labels: ["jan", "Feb", "Mar", "Apr", "May"],
				datasets: [
					{
						label: ("Oylar hisoboti"),
						data: [15, 10, 20, 5, 9],
						backgroundColor: [
							"rgba(255, 99, 132, 0.2)",
							"rgba(25, 99, 132, 0.2)",
							"rgba(45, 100, 32, 0.2)",
							"rgba(255, 99, 132, 0.2)",
							"rgba(255, 99, 132, 0.2)",
						],
						borderColor: [
							"rgba(255, 99, 132, 1)",
							"rgba(255, 99, 132, 1)",
							"rgba(255, 99, 132, 1)",
						],
						borderWidth: 1,
					},
				],
			},
		});
	},
};
</script>

<style scoped>
* {
	margin: 0;
	box-sizing: border-box;
}
</style>
