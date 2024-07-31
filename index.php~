<!DOCTYPE html>
<html lang="en">
<head>
<link rel="stylesheet" href="main.css">
<title>Generator Columns</title>
</head>

<?php
/*С помощью генераторов (yield) создать страницу, выводящую случайное число столбцов разной высоты 
(от 10% до 100% высоты экрана). Каждый столбец должен иметь случайный фон от черного до зеленого и 
содержать набор случайных символов (буквы, цифры, знаки). Использовать 2 генератора - для вывода 
самих столбцов и текста в них.
 */

function getRandomColor(){
	$i = 3;
	while($i > 0){
	$rand_color = mt_rand(0, 155);
	yield $rand_color;
	$i--;
	}
}

function getRandomSymbols($rand_height){
	$arr_symb = ['a', 'b' , 'C', 'D' , 'i' , 'F', 'g', 'h', 'i', 'J', '$', '*', '#', '!',
	      	'(', '%', '-', '+', '0', '1', '2', '3', '4', '5', '6', '7', '8', '9'];
	$str_symb = '';
	for($i = 0; $i < floor($rand_height / 3.5); $i++){
	 $str_symb .= $arr_symb[mt_rand(0, 27)] . '<br>';
         }
	yield $str_symb;
}

function getNumRandCol(){
	$num_col = mt_rand(40, 50);
	for($i = 0; $i < $num_col; $i++){
	$rand_height = mt_rand(60, 98);
	yield '<div class="columns" style="height:' . $rand_height . 'vh' . ';background:rgb('. 
		implode(', ', iterator_to_array(getRandomColor())) . ')">' . implode('<br>', iterator_to_array(getRandomSymbols($rand_height))) . '</div>';
	}
}


foreach(getNumRandCol() as $column){
	echo $column;
}
?>


<body>


</body>
</html>
