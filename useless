<?php
$file = "visitors.txt";

if (!file_exists($file)) {
    file_put_contents($file, "0");
}

$count = (int)file_get_contents($file);

if ($_GET["action"] === "join") {
    $count++;
} elseif ($_GET["action"] === "leave") {
    $count = max(0, $count - 1);
}

file_put_contents($file, $count);
echo $count;
?>
