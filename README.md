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
    </tr>
    <tr>
      <td>ដ</td>
        <td>0001011110001010</td>
    </tr>
      <tr>
      <td>ឋ</td>
        <td>0001011110001011</td>
    </tr>
      <tr>
      <td>ឌ</td>
        <td>0001011110001100</td>
    </tr>
      <tr>
      <td>ឍ</td>
        <td>0001011110001101</td>
    </tr>
      <tr>
      <td>ណ</td>
        <td>0001011110001110</td>
    </tr>
      <tr>
      <td>ត</td>
        <td>0001011110001111</td>
    </tr>
      <tr>
      <td>ថ</td>
        <td>0001011110010000</td>
    </tr>
      <tr>
      <td>ទ</td>
        <td>0001011110010001</td>
    </tr>
      <tr>
      <td>ធ</td>
        <td>0001011110010010</td>
    </tr>
      <tr>
      <td>ន</td>
        <td>0001011110010011</td>
    </tr>
      <tr>
      <td>ប</td>
        <td>0001011110010100</td>
    </tr>
      <tr>
      <td>ផ</td>
        <td>0001011110010101</td>
    </tr>
      <tr>
      <td>ព</td>
        <td>0001011110010110</td>
    </tr>
      <tr>
      <td>ភ</td>
        <td>0001011110010111</td>
    </tr>
      <tr>
      <td>ម</td>
        <td>0001011110011000</td>
    </tr>
      <tr>
      <td>យ</td>
        <td>0001011110011001</td>
    </tr>
      <tr>
      <td>រ</td>
        <td>0001011110011010</td>
    </tr>
      <tr>
      <td>ល</td>
        <td>0001011110011011</td>
    </tr>
      <tr>
      <td>វ</td>
        <td>0001011110011100</td>
    </tr>
      <tr>
      <td>ស</td>
        <td>0001011110011111</td>
    </tr>
      <tr>
      <td>ហ</td>
        <td>0001011110100000</td>
    </tr>
      <tr>
      <td>ឡ</td>
        <td>0001011110100001</td>
    </tr>
      <tr>
      <td>អ</td>
        <td>0001011110100010</td>
    </tr>
  </tbody>
</table>
