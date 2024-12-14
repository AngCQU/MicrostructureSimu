# BOXLIB_HOME defines the directory in which we will find all the BoxLib code
# If you set BOXLIB_HOME as an environment variable, this line will be ignored
BOXLIB_HOME = ../..
#MPIHOME = C:/Progra~1/MPICH2

NDEBUG    := t
MPI       := t
OMP       := 
PROF      :=
COMP      := gfortran
MKVERBOSE := t
WIN32	  := t

include ./GMakedefs.mak

include ./GPackage.mak
VPATH_LOCATIONS += .

include $(BOXLIB_HOME)/Src/F_BaseLib/GPackage.mak
VPATH_LOCATIONS += $(BOXLIB_HOME)/Src/F_BaseLib

include $(BOXLIB_HOME)/Src/LinearSolvers/F_MG/GPackage.mak
VPATH_LOCATIONS += $(BOXLIB_HOME)/Src/LinearSolvers/F_MG

main.$(suf).exe: $(objects)
	$(LINK.f90) -o main.$(suf).exe $(objects) $(libraries)

include ./GMakerules.mak
