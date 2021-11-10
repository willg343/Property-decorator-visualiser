class A:
	def __init__(self):
		self.x,self.y,self.z = range(3)

	uni_get,uni_set,uni_del=lambda self	 :	print('Universal getter'),\
							lambda self,v:	print('Universal setter:'+v),\
							lambda self	 :	print('Universal deleter')

	@property
	def a(self):
		print('Getter for a')

	@property
	def b(self):
		print("Getter for b")
	@b.deleter
	def b(self):
		print("Deleter for b")

	c = property(uni_get,uni_set,uni_del)

	d = property(None,None,fdel=uni_get)

	@property
	def e(self):
		"""doc string for e"""
		print('Getter for e')
	@e.setter
	def e(self,new_val):
		self.x=self.z=new_val

	f = property(None,uni_set)

	@property
	def g(self):
		print('Getter for g')

Obj = A()
Obj.a
del Obj.b
Obj.c = "New value"
del Obj.d
Obj.e
Obj.f = "Another Value"
Obj.g

'''
functionality:
  a: only setter
  b: getter & deletter
  c: full set (getter, setter, deleter)
  d: only deleter
  e: getter & setter
  f: only setter
  g: only getter
'''
