def trisolve(dat):
  """Solve equation a*x^2+b*x+c=0, in real domain.

      trisolve(input)input - sequence of coefficients a,b,c, returns real tuple or None tuple
      ================================
  """
  dlt = dat[1]**2-4*dat[0]*dat[2]
  if dlt >= 0:
        a2 = 2*dat[0]
        dlt = sqrt(dlt)/a2
        x0 = -dat[1]/a2
        print("x1 jest równe: ",x0-dlt)
        print("x2 jest równe: ",x0+dlt)
        return x0-dlt,x0+dlt

  else:
        print("brak pierwiastk w rzeczywistych")
        return None,None


from math import *
from configparser import *
parser = ConfigParser()
parser.read("config.rc")
sections = parser.sections()
triplets = []
for section in sections:
    for option in parser[section]:
        triplet = parser.get(section, option).split()
        x = list(map(int, triplet))
        triplets.append(x)
for triplet in triplets:
    print(triplet)
    trisolve(triplet)
