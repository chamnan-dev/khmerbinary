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
<p>Khmer binary code</p>
<table>
  <thead>
    <tr>
      <th>Khmer alphabet</th>
      <th>Khmer binary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>ក</td>
    </tr>
    <tr>
      <td>ខ</td>
    </tr>
    <tr>
      <td>ឃ</td>
    </tr>
  </tbody>
</table>
