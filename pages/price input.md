-
- ```dart
  import 'package:intl/intl.dart';
  
  void main() {
    addThousandSeparatorText('34,567,890');
    print('---------');
    addThousandSeparatorText('34,567,890.');
    print('---------');
    addThousandSeparatorText('34,567,890.12');
    print('---------');
    addThousandSeparatorText('.12');
  }
  
  void addThousandSeparatorText(String text) {
    final f = NumberFormat('#,###');
    final String allText = text;
    print('allText: $allText');
  
    // eg: 34,567,890.12 -> 34567890.12
    final allTextWithoutDecimalComma =
        allText.replaceAll(f.symbols.GROUP_SEP, '');
    print('allTextWithoutDecimalComma: $allTextWithoutDecimalComma');
  
    // eg: 34567890.12 -> index = 8
    // eg: 34567890 -> index = -1
    final decimalPointIndex = allTextWithoutDecimalComma.indexOf('.');
    print("decimalPoint index: $decimalPointIndex");
  
    final String digitsText;
    final String decimalText;
  
    if (decimalPointIndex != -1) {
      digitsText = allTextWithoutDecimalComma.substring(0, decimalPointIndex);
      decimalText = allTextWithoutDecimalComma.substring(
          decimalPointIndex, allTextWithoutDecimalComma.length);
    } else {
      digitsText = allTextWithoutDecimalComma;
      decimalText = '';
    }
  
    print('digitsText: $digitsText');
    print('decimalText: $decimalText');
  
    final String digitsTextWithDecimalComma;
    if (digitsText.isNotEmpty) {
      final digitsNumber = int.parse(digitsText);
      digitsTextWithDecimalComma = f.format(digitsNumber);
    } else {
      digitsTextWithDecimalComma = '';
    }
  
    print('digitsTextWithDecimalComma: $digitsTextWithDecimalComma');
  
    final newText = digitsTextWithDecimalComma + decimalText;
    print('newText: $newText');
  }
  ```