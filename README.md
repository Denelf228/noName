# noName
class Triangle(object):
  def __init__(self, a, b, c, a_gr, b_gr, c_gr):
    self.a = a #сторона
    self.b = b #сторона 
    self.c = c #сторона
    self.a_gr = a_gr #угол
    self.b_gr = b_gr #угол
    self.c_gr = c_gr #угол
  def perimeter(self):
    return self.a + self.b + self.c
  def square(self):
    import math
    return ((self.a * self.b) / 2) * math.sin(self.a_gr)
  def typeoftriangle(self):
    if self.a == self.b == self.c and (self.a_gr == 90 or self.b_gr == 90 or self.c_gr == 90):
      return 'Равносторонний'
    elif (self.a == self.b) and (self.a_gr == 90 or self.b_gr == 90 or self.c_gr == 90):
      return 'Равнобедренный и прямоугольный'
    elif (self.b == self.c) and (self.a_gr == 90 or self.b_gr == 90 or self.c_gr == 90):
      return 'Равнобедренный и примоугольный'
    elif (self.a == self.c) and (self.a_gr == 90 or self.b_gr == 90 or self.c_gr == 90):
     return 'Равнобедренный и прямоугольный'
    elif self.a == self.b:
     return "Равнобедренный"
    elif self.b == self.c:
     return "Равнобедренный"
    elif self.a == self.c:
      return 'Равнобедренный'
    else:
      return 'Разносторонний'
    
nuw_tr = Triangle(float(input()), float(input()), float(input()), float(input()), float(input()), float(input()))
print(nuw_tr.perimeter())
print(nuw_tr.square())
print(nuw_tr.typeoftriangle())
