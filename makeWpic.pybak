def makeWpic():
  fname=pickAFile()
  pic=makePicture(fname)
  gpic=duplicatePicture(pic)
  nepic=duplicatePicture(pic)
  spic=duplicatePicture(pic)
  w=getWidth(pic)
  h=getHeight(pic)
  npic=makeEmptyPicture(w*2,h*2)
  copyInto(pic,npic,0,0)
  copyInto(grayScale(gpic),npic,w,0)
  copyInto(negative(nepic),npic,0,h)
  copyInto(swapPic(spic),npic,w,h)
  show (npic)
def grayScale(gpic):
  for p in getPixels(gpic):
    intensity=(getRed(p)+getGreen(p)+getBlue(p))/3
    setColor(p,makeColor(intensity,intensity,intensity))
  return (gpic)

def negative(nepic):
  for px in getPixels(nepic):
    red=getRed(px)
    green=getGreen(px)
    blue=getBlue(px)
    negColor=makeColor(255-red, 255-green, 255-blue)
    setColor(px,negColor) 
  return (nepic)

def swapPic(spic): 
  for p in getPixels(spic):
    red=getRed(p)
    green=getGreen(p)
    blue=getBlue(p)
    color= makeColor(blue,red,green)
    setColor(p,color)
  return (spic)
