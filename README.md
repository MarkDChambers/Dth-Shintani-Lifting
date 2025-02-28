There are two folders - one that uses quadratic twists, and the other that uses generators of the dirichlet group in the relevant cyclotomic extension.

However, both have exactly the same structure, and are almost identical.

Specifically, there are 5 files - **Test_(Cyclotomic/Quadratic), KojimaTokuno, QFBasis, Pell, PMBasis**. The function of these are

**Test_(Cyclotomic/Quadratic)**: The high-level program that is run, conducting the test, but does few calculations itself. It iterates through modular forms, calculates
the different tuples/classes for the fundamental discriminants, and then pulls the requests the relevant lift from KojimaTokuno

**KojimaTokuno**: This closely follows the formula you would see in the paper of Kohen, Kojima-Tokuno, requesting QFBasis, Pell to do the subtasks

**QFBasis**: Calculates a set of representatives for L_Nt(D)/\Gamma_0(N)

**Pell**: Calculates the minimal positive solution to x^2-Dy^2=4 for D a discriminant

**PMBasis**: Generates the basis for the plus and minus subspaces of the modular symbol space associated to a newform f

**IMPORTANT NOTE**: The output of the code appears to be consistent for mth coefficients where \chi(-1)(-1)^k m is a fundamental discriminant, but when this is a discriminant, the output is very unreliable
