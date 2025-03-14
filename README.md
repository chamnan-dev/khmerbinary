<head>
    
<link href="style.css" rel="stylesheet">
</head>


<img src="khmerbinary.png" alt="khmer binary code">

# Convert Khmer Text To Binary Code With PHP

Example below show you about khmer text to binary code by create function and called it.


```php
<?php
function khmerToBinary($khmerText) {
    $binaryString = '';
    
    // Convert each character to Unicode code point
    for ($i = 0; $i < mb_strlen($khmerText, 'UTF-8'); $i++) {
        $char = mb_substr($khmerText, $i, 1, 'UTF-8');
        $codePoint = mb_ord($char, 'UTF-8'); // Get the Unicode code point
        
        // Convert the code point to binary
        $binary = decbin($codePoint);
        
        // Append the binary representation to the string
        $binaryString .= str_pad($binary, 16, '0', STR_PAD_LEFT); // Pad to 16 bits
    }
    
    return $binaryString;
}

// Example usage
$khmerText = "សួស្ដី"; // "Hello" in Khmer
$binaryOutput = khmerToBinary($khmerText);
echo $binaryOutput;
?>

```

# Convert Binary To Khmer Text With PHP code.

```php
<?php
function binaryToKhmer($binaryString) {
    $khmerText = '';

    // Split the binary string into chunks of 16 bits (or more if needed)
    $binaryChunks = str_split($binaryString, 16);

    foreach ($binaryChunks as $binary) {
        // Convert binary to decimal (Unicode code point)
        $codePoint = bindec($binary);

        // Convert the code point to a character
        $char = mb_chr($codePoint, 'UTF-8'); // Get the character from the code point

        // Append the character to the resulting text
        $khmerText .= $char;
    }

    return $khmerText;
}

// Example usage
$binaryInput = "0001011110000000"; // Example binary string
$khmerText = binaryToKhmer($binaryInput);
echo $khmerText;
?>



```

<p>Khmer binary code</p>
<table>
  <thead>
    <tr>
      <th>Khmer alphabet</th>
      <th>Khmer binary</th>
      <th>Khmer alphabet</th>
      <th>Khmer binary</th>
      <th>Khmer alphabet</th>
      <th>Khmer binary</th>
      <th>Khmer alphabet</th>
      <th>Khmer binary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>ក</td>
      <td>0001011110000000</td>
        <td>ខ</td>
        <td>0001011110000001</td>
        <td>គ</td>
        <td>0001011110000010</td>
        <td>ឃ</td>
        <td>0001011110000011</td>
    </tr>
    <tr>
      <td>ង</td>
        <td>0001011110000100</td>
        <td>ដ</td>
        <td>0001011110001010</td>
        <td>ឋ</td>
        <td>0001011110001011</td>
        <td>ឌ</td>
        <td>0001011110001100</td>
    </tr>
      <tr>
      <td>ឍ</td>
        <td>0001011110001101</td>
        <td>ណ</td>
        <td>0001011110001110</td>
         <td>ត</td>
        <td>0001011110001111</td> 
        <td>ថ</td>
        <td>0001011110010000</td>
    </tr>
      <tr>
      <td>ទ</td>
        <td>0001011110010001</td>
        <td>ធ</td>
        <td>0001011110010010</td>
          <td>ន</td>
        <td>0001011110010011</td>
        <td>ប</td>
        <td>0001011110010100</td>
    </tr>
      <tr>
      <td>ផ</td>
        <td>0001011110010101</td>
          <td>ព</td>
        <td>0001011110010110</td>
          <td>ភ</td>
        <td>0001011110010111</td>
          <td>ម</td>
        <td>0001011110011000</td>
    </tr>
      <tr>
      <td>យ</td>
        <td>0001011110011001</td>
          <td>រ</td>
        <td>0001011110011010</td>
          <td>ល</td>
        <td>0001011110011011</td>
          <td>វ</td>
        <td>0001011110011100</td>
    </tr>
      <tr>
      <td>ស</td>
        <td>0001011110011111</td>
        <td>ហ</td>
        <td>0001011110100000</td>
        <td>ឡ</td>
        <td>0001011110100001</td>
          <td>អ</td>
        <td>0001011110100010</td>
    </tr>
  </tbody>
</table>
