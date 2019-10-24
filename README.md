### urwid
---
https://github.com/urwid/urwid

http://urwid.org/

```py
// test_text_layout.py

class CalcBreaksTest(object):
  def cbtest(self, width, exp):
    result = text_layout.default_layout.calculate_text_segments(
      B(self.text), width, self.mode )
    assert len(result) == len(exp), repr((result, exp))
    for l, e in zip(result, exp):
      end = l[-1][-1]
      assert end == e, repr((result,exp))
  
  def test(self):
    for width, exp in self.do:
      self.cbtest( width, exp )

class CalcBreaksCharTest(CalcBreaksTest, unittest.TestCase):
  mode = 'any'
  text = "xxx"
  do = [
    (),
    (),
    (),
  ]
  
class CalcBreakDBCharTest(CalcBreaksTest, unittest.TestCase):
  def setUp(self):
    urwid.set_encoding("euc-jp")
  
  mode = 'any'
  text = "xxx"
  do = [
    (),
    (),
    (),
  ]

```

```
```

```
```


