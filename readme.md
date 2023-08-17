### scalePoint : 간격에 맞게 값을 변경해줍니다.

const f1 = d3.scalePoint().range([0, 100]).domain([10, 12, 20, 30, 40]);
console.log(f1(12));

const f2 = d3.scalePoint().range([0, 100]).domain(["a", "b", "c", "d"]);
console.log(f2("b"));

### scaleLinear : 비율에 맞게 값을 변경해줍니다.

const f1 = d3.scaleLinear().range([0, 100]).domain([0, 500]);
console.log(f1(250));
console.log(f1(0));
console.log(f1(500));
console.log(f1(1000));

crayons = d3
.scaleLinear()
.domain([-1, 0, 1])
.range(["orange", "white", "green"]);
console.log(crayons(-0.2));

### scaleBand : 숫자가 아니라 키값으로 찾을 수 있게 해줍니다.

const f = d3
.scaleBand()
.domain(["one", "two", "three", "four"])
.range([0, 100]);

console.log(f("one"));
console.log(f("two"));
console.log(f("three"));
console.log(f("four"));
console.log(f.bandwidth());
