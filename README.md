# maximum-weight-difference

<?php
function calculateWeightDiff($arr, $k) {
    sort($arr); 
    $chefweight = 0;
    $sonweight =0;

for($i=0;$i<count($arr);$i++){
 if($i<$k){
    $sonweight=$sonweight+$arr[$i];
  } else{
    $chefweight=$chefweight+$arr[$i];
  }
}
return abs($chefweight-$sonweight);
}
$testcase=[
    [[8,4,5,2,10],2],
    [[1,1,1,1,1,1,1,1],3]
];

foreach ($testcase as $testcase) {
    # code...
    $arr=$testcase[0];
    $k=$testcase[1];
    $result=calculateWeightDiff($arr,$k);
    echo "Maximum Weight Difference:". $result ."grams\n";
}
?>
