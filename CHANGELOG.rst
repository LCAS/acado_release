^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package acado
^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.2.3 (2017-05-19)
------------------
* added missing package.xml
* Merge pull request `#161 <https://github.com/LCAS/acado/issues/161>`_ from clearpathrobotics/CORE-1683_spam_fix
  Commented out a message that gets displayed even when PRINTLEVEL is set to NONE
* minor update lifted adjoint integrator
* correction of the adjoint term
* removed the option LIFTED_INTEGRATOR_MODE
* implemented INIS scheme with adjoint correction
* adjoint exact Hessian solver
* fixed bug regarding gradient update in exact Hessian RTI
* adjoint gradient update for qpdunes interface
* nasty bug found in expansion step for multipliers
* no timing functionality in the S-function in case of _DSPACE
* compilation problem in auto generated S functions
* initialize in auto generated S-function
* modulePrefix support in auto generated S-functions
* unnecessary whitespace in make script for auto generated S-function
* fixed important bug regarding online data and controls entering constraints or objective, but not model equations (sensitivities are still propagated for such slack variables though) `#79 <https://github.com/LCAS/acado/issues/79>`_
* FOA equations within standard implicit integrators
* fixed qpdunes interface
* fix FORCES Pro interface
* fix FORCES Pro interface
* robot simulink example
* fix crane example
* updated code generated licensing information
* fixed IRK with FOB sensitivity propagation
* no gradient update by default
* standard collocation integrator with symmetric Hessian propagation
* transpose linear system reuse for simplified newton iterations
* fixed bugs in Sfunction interface coming from `#177 <https://github.com/LCAS/acado/issues/177>`_
* minor update of MEX inteface EH solver
* module names fix in sfunction interface `#177 <https://github.com/LCAS/acado/issues/177>`_
* fixed double module names for regularization
* missing module names
* prefix linear solvers lifted IRK `#177 <https://github.com/LCAS/acado/issues/177>`_
* moduleName missing in export NLP solver `#177 <https://github.com/LCAS/acado/issues/177>`_
* undo two accidental changes by PR `#177 <https://github.com/LCAS/acado/issues/177>`_
* Merge pull request `#177 <https://github.com/LCAS/acado/issues/177>`_ from ferreau/withModuleName
  implemented CG_MODULE_NAME feature (also relying on CG_MODULE_PREFIX)…
* fixed the matlab makehelper for Visual Studio 2015 `#179 <https://github.com/LCAS/acado/issues/179>`_
* Merge branch 'master' into withModuleName
* bug fixes from pull request `#176 <https://github.com/LCAS/acado/issues/176>`_
* implemented CG_MODULE_NAME feature (also relying on CG_MODULE_PREFIX) allowing to customize the prefix for all functions/variables in global scope; this allows the user to compile multiple exported controllers into a single executable; feature not yet implemented for all solver/algorithm variants, but should be backwards compatible if CG_MODULE_NAME is set to "acado" and CG_MODULE_PREFIX to "ACADO".
* Merge pull request `#176 <https://github.com/LCAS/acado/issues/176>`_ from ferreau/latestQpoases
  added qpOASES-3.2.0 for standard ACADO and qpOASES_e-3.1.1 for ACADO …
* added missing template entry for qpOASES3
* final corrections
* added qpOASES-3.2.0 for standard ACADO and qpOASES_e-3.1.1 for ACADO CGT; few more tiny adjustments to make code compile under cygwin
* added qpOASES-3.2.0 for standard ACADO and qpOASES_e-3.1.1 for ACADO CGT; few more tiny adjustments to make code compile under cygwin
* static nonlinear feedback integrators
* more accurate code generation of constant values in the model equations
* implemented an adjoint SQP method
* implemented an adjoint SQP method
* lifted ERK methods interface update
* initial cleanup and bug fixing for lifted IRK methods
* lifted ERK methods
* use lifted gradient update by default
* Windows fix in response to issue `#168 <https://github.com/LCAS/acado/issues/168>`_ `#171 <https://github.com/LCAS/acado/issues/171>`_ and merging with `#172 <https://github.com/LCAS/acado/issues/172>`_
* Merge pull request `#172 <https://github.com/LCAS/acado/issues/172>`_ from andresbh/master
  msvc2015 compiler check
* msvc2015 compiler check
* export of declarations for externally defined model functions `#166 <https://github.com/LCAS/acado/issues/166>`_
* added argument for externally generated C files for generated make scripts when using OCPexport `#166 <https://github.com/LCAS/acado/issues/166>`_
* fixed bug regarding example crane_closed_loop in mpc_mhe folder of code generation examples
* made the symmetric and FOB lifted integrator implementation comparable
* implementation of gradient updates for exact Hessian based lifted collocation
* LIFTED_GRADIENT_UPDATE added to options list
* collocation equivalent propgation of constant values
* minor bug when only one integration step for lifted schemes
* gradient computation for lifted symemtric collocation scheme
* minor bug fix in symmetric IRK methods
* minor improvement AD for SYM based IRK method
* minor improvement AD for FOB based IRK method
* minor improvement AD for FOB based ERK method
* minor improvement AD for 3sweep ERK method
* improved efficiency of FOA scheme for ERK methods
* made the order of sensitivities in FOA scheme of ERK methods consistent with the TSP scheme
* commented out the error code computation for lifted schemes
* bug fix regarding the order of the derivatives in EH-RTI schemes
* don't stop simulation when ret ~= 0
* implemented regularization of condensed Hessian for EH-RTI
* implemented transposed single Newton solver for 3 stage IRK methods
* implemented the lifted FOB integrator
* renaming of THREE_SWEEPS --> SYMMETRIC
* finished symmetric IRK methods
* liftMode == 4 means INEXACT Newton based schemes
* solution of transposed linear systems using IRK_GL8 single Newton type solver
* development of lifted integrators with symmetric Hessian propagation
* renaming of THREE_SWEEPS to SYMMETRIC
* transposed linear system solves using Gauss elimination
* renaming of THREE_SWEEPS to SYMMETRIC
* stage point constraints in MATLAB interface
* Merge branch 'stable' of github.com:acado/acado
* replaced WIN32 by _WIN32
* minor update robot example
* fixed important bug regarding complex constraints and N2 condensing
* bug fix regarding complex constraints in N2 condensing
* FORWARD_OVER_BACKWARD implementation with Exact Hessian based RTI
* FORWARD_OVER_BACKWARD implementation with Exact Hessian based RTI
* minor bug fix regarding full condensing for MHE
* redefinition of register keyword unnecessary on Windows systems
* merge of stable with master branch to maintain a more stable version of most code generation features (documentation to be updated)
* Merge pull request `#132 <https://github.com/LCAS/acado/issues/132>`_ from tibnor/stable
  Fixed evaluation of lsq term when there is only one (time)point.
* Merge pull request `#131 <https://github.com/LCAS/acado/issues/131>`_ from tibnor/master
  Fixed evaluation of lsq term when there is only one (time)point.
* CORE-1683: Commented out a printf that spammed GDB with meaningless message even when PRINTLEVEL is set to NONE.
* Merge pull request `#2 <https://github.com/LCAS/acado/issues/2>`_ from acado/stable
  Stable
* stupid typo in make script
* throw error for exact hessian based solver and LSQ objectives
* Merge branch 'master' of github.com:rienq/acado
* slight modification of error message
* typo
* bug fix regarding complex point constraints
* MULTIPLE SHOOTING is default option
* support for complex constraints in exact hessian based SQP
* implemented path and point constraints for N2 condensing
* update of makefile for qpdunes
* -fPIC compiler option with qpDUNES
* compare pointers instead of std::ostream objects
* remove register keyword in case of clang compiler
* Cmake additions related to tr1 namespace and headers
* removed some warnings
* update MATLAB make script after tr1 update
* removed tr1 namespace and headers because of recent problems on OS X
* minor bug fix for quadcopter simulation example
* bug fix regarding linear input states and the order of differential equations in code generation
* pass errors in case of false modelData when using SIMexport
* order of explicitly defined differential equations and order of state variables should correspond such that no reordering is needed
* error message when defining implicit system for ERK method
* update integrator MEX in case no control inputs are defined
* Merge pull request `#159 <https://github.com/LCAS/acado/issues/159>`_ from clearpathrobotics/CPR_perfs
  If PRINTLEVEL = NONE, do not display RET_MAX_NUMBER_OF_STEPS_EXCEEDED.
* Added so that if PRINTLEVEL is set to NONE, maximum-number-of-iterations-exceeded message is not displayed. Helpful for online multiple calls to the solver.
* fixed order variables in case of DAE in sfunction interface `#151 <https://github.com/LCAS/acado/issues/151>`_
* fixed bug related to memcopy, because of dummy variable, in the Simulink interface `#151 <https://github.com/LCAS/acado/issues/151>`_
* bug fix in Mayer term evaluation for EMPC when defining online data `#155 <https://github.com/LCAS/acado/issues/155>`_
* Merge pull request `#1 <https://github.com/LCAS/acado/issues/1>`_ from acado/stable
  Updated stable branch to pull in Shahab's performance improvements
* Merge pull request `#156 <https://github.com/LCAS/acado/issues/156>`_ from clearpathrobotics/CPR_perfs
  Some performance improvements for when OCP is called in a loop
* bug fix MATLAB interface regarding setting dimensions explicitly
* Reverted back the condense freezing so as to not cause test files to fail.
* Relocated SVD computation if LOG level is true (or else it would do SVD when it is not needed). Improves performance if OCP is called recursively in a loop.
* Re-enabled condense-freezing for QPs
* important fix for preparation step of qpDUNES with block condensing
* simplified and single newton scheme for 8th order Gauss method
* bug fix inexact Newton based lifted integrators
* bug fix single newton scheme
* support for implicit DAEs in lifted IRK integrators
* cherry pick of 62adb033ef3ef273801767faa8770df266971cca into stable
* Merge branch 'master' of github.com:acado/acado
* return number of iterations with qpDUNES solver from MEX interface
* return number of iterations from FORCES in MEX interface
* important compiler flag for getting FORCES output information
* Merge branch 'master' of github.com:acado/acado
* Merge branch 'master' of github.com:acado/acado
* Merge pull request `#148 <https://github.com/LCAS/acado/issues/148>`_ from rafaelsaback/patch-1
  Correcting comment from integers to booleans
* Correcting comment from integers to booleans
* minor code improvements when using block condensing with blocksize == 1
* fix regarding issue `#145 <https://github.com/LCAS/acado/issues/145>`_
* MEX interface for FORCES + block condensing
* update of block condensing solver with FORCES
* attemp to fix issue `#145 <https://github.com/LCAS/acado/issues/145>`_
* block condensing for FORCES
* block condensing for FORCES
* block condensing for FORCES
* block condensing for FORCES
* LVL_DEBUG for OCPexport and SIMexport in MATLAB
* block condensing for FORCES
* block condensing for FORCES
* Merge pull request `#146 <https://github.com/LCAS/acado/issues/146>`_ from rafaelsaback/patch-1
  Changed qpoases_interface.cpp.in include in order to search for acado_common.h locally
* acado_common.h include
  Hey guys,
  I'm changing the acado_common.h include in order to search for the file locally. I've been getting a linkage error when exporting the code and I had to change it manually everytime.
* throw matlab error when code generation fails in SIMexport `#141 <https://github.com/LCAS/acado/issues/141>`_
* throw an error when something goes wrong setting an option `#141 <https://github.com/LCAS/acado/issues/141>`_
* Merge branch 'master' of github.com:rienq/acado
* exact embedded collocation
* Merge branch 'master' of github.com:rienq/acado
* renaming of IRK solver and single Newton scheme
* towards block condensing with FORCES
* minor bug fix block condensing
* throw error when ACADO failed to export code `#141 <https://github.com/LCAS/acado/issues/141>`_
* Merge branch 'stable' of github.com:acado/acado
* bug fix regarding time depending constraints in MATLAB interface
* block condensing with various qp solvers
* FORCES and mixed state-control weighting terms
* FORCES and objective state-control cross weighting terms
* update of matlab examples
* update of addTemplates script
* merge master Milan
* Merge branch 'master' of https://github.com/acado/acado
* fixed datenum issue in MATLAB interface
* fix for externally defined residual functions and state-control cross terms
* Merge branch 'master' of https://github.com/acado/acado
* hpmpc mpc interface update
* OnlineData varying over horizon  `#134 <https://github.com/LCAS/acado/issues/134>`_
* acado_hessian_regularization.c in MakeFile `#134 <https://github.com/LCAS/acado/issues/134>`_
* OnlineData varying over horizon  `#134 <https://github.com/LCAS/acado/issues/134>`_
* update of the lifted integrators with tailored IRK linear solvers
* allow export of tailored IRK linear solvers, using complex arithmetics in generated code
* allow export of tailored IRK linear solvers, using complex arithmetics in generated code
* allow export of tailored IRK linear solvers, using complex arithmetics in generated code
* allow export of tailored IRK linear solvers, using complex arithmetics in generated code
* externally defined residual functions in ACADO from MATLAB
* externally defined residual functions in ACADO from MATLAB
* first implementation of the lifted integrator
* lifted integrator mode
* call to lifted integrator
* lifted integrator mode
* integrator constants defined in acado_common header
* getIntegrationGrid
* no timings on DSPACE hardware
* bug fix MHE + forces
* Newton initialization fix for algebraic variables in DAEs
* fixed typo in S-function generator
* split QPdunes timings for block condensing
* Fixed evaluation of lsq term when there is only one (time)point.
  Conflicts:
  acado/objective/lsq_term.cpp
* splitting qpDUNES call in preparation and feedback phase for block based condensing RTI solver
* splitting qpDUNES call in preparation and feedback phase for block based condensing RTI solver
* Fixed evaluation of lsq term when there is only one (time)point.
  Conflicts:
  acado/objective/lsq_term.cpp
* typo in MEX interface
* non hardcoded bound values for FORCES and MEX interface
* non hardcoded bounds for block condensing based RTI solver with qpDUNES
* non hardcoded bounds for block condensing based RTI solver with qpDUNES
* variable bounds for block condensing based solver
* delete of deprecated QPDUNES2
* fixed warning
* setters in ModelContainer of MATLAB interface
* initialization of bounds for qpDUNES when not hardcoded
* initialize bounds qpDUNES in MEX interface
* initialize bounds qpDUNES
* non hardcoded constraints for qpDUNES
* non hardcoded constraints for qpDUNES
* non hardcoded constraints for qpDUNES
* problem online data detection outside of model
* always have lbValues and ubValues when not hardcoding constraints, otherwise bug in MEX interface
* print level for block based condensing + qpdunes
* update compiler flags for qpdunes-dev
* support for nonequidistant grids in ACADO MATLAB codegen
* revert 32ad2ca7059ac2034221b7348108d267cfb2a37e
* verbose option for MATLAB interface make script
* Slx and Slu support in MATLAB interface
* updated flags for qpDUNES-dev solver
* fixed bug dual solution
* bug fix in the expand of the last of the block condensing
* minor bug fix in case of block size == 1
* changed default compiler for development branch of qpdunes
* fixed block based condensing of state bounds
* added new template
* fixed kkt evaluation for block based condensing
* implemented block based condensing with qpDUNES
* update qpDUNES interface
* minor bug fix in N2 condensing
* Merge branch 'master' of https://github.com/acado/acado into stable
* fixed assert problem raised by powerkite example (2)
* Merge branch 'master' of https://github.com/acado/acado into stable
* fixed assert problem raised by powerkite example
* merge of master into stable branch
* Working on HPMPC MHE solver
* fixed typo in makefiles matlab
* Compiler flag -DWIN32 added because it does not always seem to be defined by default, depending on the compiler and MATLAB version in Windows
* Fixing of the MATLAB interface for Windows and MATLAB R2014a/b
* regularization of the NX part of the Hessian
* regularization of the NX part of the Hessian
* regularization of the NX part of the Hessian
* bug fix regarding state bounds in N2 condensing when initial state is not fixed
* state constraints in N2 condensing with initial state free
* N2 partial condensing for MHE and time optimal OCP
* S-function make script minor fix
* typo in N2 condensing
* solved two nasty bugs in N2 condensing, regarding S1 terms
* minor bug fix in qpDUNES interface
* fix for stable version of qpDUNES
* update economic powerkite example
* only full condensing yet in case initial state is fixed
* solved two nasty bugs in N2 condensing, regarding S1 terms
* update of N2 condensing to newest version
* minor bug fix because of qpDUNES-dev
* minor bug fix regarding Hessian regularization function
* update of initialization in case of exact Hessian RTI using qpDUNES
* fix of qpDUNES interface for dense Hessians
* levenberg marquardt terms for exact Hessian based RTI using qpDUNES
* Fixing arrival cost computation; temporary one
* Minor fixed in export of an arith. statement
* update of the templates in the MATLAB interface
* update of the Exact Hessian based OCP solver using qpDUNES
* new MEX Makefile for the Exact Hessian based RTI solver using qpDUNES
* renaming of acadoCopyTempateFile to acadoCopyTemplateFile
* compiler C flag for C++ style comments in qpDUNES
* passing of lagrange multipliers to the user
* renaming of utils --> qpdunes_utils in make script
* Merge branch 'master' of github.com:mvukov/acado
* exact Hessian based RTI using qpDUNES
* cleanup of exported OCP solvers for more exact Hessian based algorithms
* renaming of the condensing based Exact-Hessian RTI solver
* Added skeleton for warm-starting FORCES
* update of the MATLAB interface after moving source and header files `#122 <https://github.com/LCAS/acado/issues/122>`_
* Added options to warm start FORCES
* HPMPC wrapper update
* Fixed default options for FORCES based OCP solver:
  - init set to 0 as before
  - mu0 set to 1.0 (this happens to be an old setting)
  Those settings should "almost" resamble the old settings from 2012.
* Decreasing tolerance for HPMPC OCP solvers
* Fixing the default settings for the FORCES OCP solvers
* Minor bug fix in the HPMPC OCP solver
* Fixed a minor bug in the nlp export class
* Fixing OCP qpDUNES
* OCP based on HPMPC stuff updated
* Fixing header inclusion in the qpdoomed based ocp solver
* Fixed computations for KKT tolerance with qpDOOMED based OCP solver
* Removed a stupid warning
* Interfaced multipliers from HPMPC interfaces and now compute KKT tol.
* Added KKT tolerance calc to the qpDUNES based OCP solvers
* Ups, fixing a typo...
* Fixing the previous mess
* Disabled temporarily the OSX build on Travis-CI
* Extending the qpDUNES interface to support MHE, `#59 <https://github.com/LCAS/acado/issues/59>`_
  Under dev, has to be tested
* Fixing sparsity exploitation in the export_nlp_solver
* Moved bindings from external_packaged folder to the main src tree
* Moved bindings to external packages to the main src tree
* Cleaning the FORCES interface
  - No more support for single shooting
  - Cleanup of some dead and invalid code
  - Preparation for extension for MHE
* Trying out multi OS support
* fixed a bug in the build system and made install paths relative again
* Further cleaning of the build system
* Restructured the main source tree and update the build system
* Updated CMake stuff; added some macros
* Changed the header inclusion the empc powerkite example.
* Removing assert from Expression's assigmentSetup
* Merge branch 'master' of git://github.com/rienq/acado
* bug fix towards fixing issue `#111 <https://github.com/LCAS/acado/issues/111>`_
* added reset functionality to the integrator MEX interface
* added reset functionality to the integrator MEX interface
* fix MATLAB interface to solve `#107 <https://github.com/LCAS/acado/issues/107>`_
* fix MATLAB interface to solve `#107 <https://github.com/LCAS/acado/issues/107>`_
* changed the fix for `#112 <https://github.com/LCAS/acado/issues/112>`_ to only affect Windows users in an attempt to fix `#121 <https://github.com/LCAS/acado/issues/121>`_ for Mac users
* Removing redundant operator<< from the expression class
* fix qpOASES interface regarding `#108 <https://github.com/LCAS/acado/issues/108>`_
* fixed a fix in makehelper.m
* solved compiler issue with long commands to linker on Windows `#112 <https://github.com/LCAS/acado/issues/112>`_
* Moved constraints stuff from expression class to constraint_component
* Merge branch 'master' of github.com:mvukov/acado
* Cleaning the symbolics API
* Disabling examples with appveyor
* Updated README.md
* Merge branch 'issue_111' of github.com:mvukov/acado
* Ignoring some warnings with MSVS
* Merge branch 'issue_111'
* Fixed SVD tutorial test
* Merge branch 'master' of https://github.com/acado/acado
* Merged with mvukov/issue_111. Builds and runs on Win and Linux
* powerkite_on.cpp example fails, move it to dev
* Trying to fix the powerkite_on.cpp example
* Fixing parameter_estimation_tutorial2.cpp example
* Fixing the fourtankNMPC.cpp example
* powerkite_on.cpp example fails, move it to dev
* Trying to fix the powerkite_on.cpp example
* Fixing parameter_estimation_tutorial2.cpp example
* Fixing the fourtankNMPC.cpp example
* Fixing the symbolics API, issue `#111 <https://github.com/LCAS/acado/issues/111>`_
* Merge branch 'master' of github.com:mvukov/acado into issue_111
* Fixing a6054de.
* Revert "Making Hessian symmetric changed from warning to info."
  This reverts commit a6054deb8a07366f704612c0502e280b85addbde.
* Merge branch 'master' of github.com:mvukov/acado into issue_111
* If testing is ON, warnings are considered as a failure.
* Making Hessian symmetric changed from warning to info.
* ACADO qpOASES compilation problem^C
* Added the updated interface to HPMPC
* added FORCES Python interface to MATLAB interface
* MSVC build errors fixed
* Merged with mvukov/issue_111, did some small fixes -- now it compiles under MSVC!
* Refactored symbolics API; beware leaking memory like crazy
* * Removed "using Base::operator=" from GenericMatrix<> and GenericVector<>. They caused build errors under MSVC. Compiler-generated operator= should be fine.
  * Changed "or" and "and" to "||" and "&&" operators. Not all compilers understand "or" and "and".
  * Added missing header <algorithm> to interval.ipp
  * Fixed MSVC build error in vector.cpp
  * Removed "using namespace std" in objective.cpp, which was causing another build error under MSVC.
* Cleaned header inclusion in the CGT.
* Merge branch 'master' of github.com:acado/acado
  Conflicts:
  src/code_generation/export_common_header.cpp
* Tests should run now as expected, not allowed to fail any more
* example with bdf updated
* BDF revived in a dodgy way
* Cleaning headers: function
* cleaning the headers
* Update for the FORCES interface...
  - Added an option, CG_FORCE_DIAGONAL_HESSIAN, to manualy force diagonal
  struct of the stage Hessians. This cannot be exploited atm
  automatically if external AD is used (like we do it in rawesome).
  - Python and MATLAB generators are updated accordingly.
* Forces interface updated...
  - added C++ guards to the interface snippet
  - The makefile calls the Python generator now by default
* Added Python generator for FORCES QP solver.
* changed comments in qpdunes interface
* changed comments in qpdunes interface
* matlab NMPC example codes copy the qpoases solver
* copy of the qpoases solver for the crane example
* Fixing LM in HPMPC GN based solver
* Fixed objective evaluation in the qpDUNES GN OCP solver
* Trying to fix c71cda077f5b28956ab1e3810dc733d7b7b28746
* qpDUNES interface: log levels are again set from ACADO...
  ... and not hardcoded to None.
* Suppress some shitty warnings from CMake 3.0
* Removing qpDunes.h inclusion from the generated acado_common.h
* added EMPC example for exact hessian based RTI
* reverted an accidentally removed comment from Milan in the code
* update of addTemplates.m
* removed some warnings in expression class
* merged addTemplates.m
* merge with acado master
* added a new class which exports an exact-hessian based RTI scheme, using N2 condensing and qpoases
* new friend class for Hessian regularizations
* added getRows and getCols functionality to expression class
* a few extra useful getters for objective class
* a few extra useful getters for objective class
* update templates folder for new exact hessian related templates
* EQUALITY_EPS at least a bit smaller
* update
* added new templates for exact hessian based RTI, including an EVD based Hessian regularization
* Updated matrix and vector printing plus export of data declarations in the CGT...
  - Matrix and vector printing: update. Default for non-double, special instantiation
  for matrix and vector of doubles
  - Export variables of type STATIC_CONST_INT or _REAL are _not\_ given any more. This
  allows for some better optimizations when those guys contain big/huge arrays.
* Fixing the HPMPC interface
* use of getElement more often
* HPMPC interface made configurable
* Updated HPMPC interface for non-constant stage Hessians
* Merge branch 'master' of github.com:mvukov/acado
* Working on `#107 <https://github.com/LCAS/acado/issues/107>`_
* travis: c++ -> cpp
* Fixing b76ca80
* Cleaning the headers.
* Refactored OCP class...
  ... Simplified header inclusion
* Added option to build only the CGT...
  ... and corresponding examples.
  The option is OFF by default
* Fixed acado axu fcns for mingw
* Adding support to cross compile with mingw
* Simplified registration of the exported integrators.
* Added the appveyor script
* Added a function to get error string from embedded qpOASES
* Rearranged and cleaned the headers in the SIMexport class
* khm, another fix
* Fixing a stupid bug.
* Cleaned some headers
* Fixed addTemplate.m (matlab interface)
* Merge branch 'master' of github.com:acado/acado
* Another set of simplification of the build system
  - code_generation.hpp includes only public classes headers. This should
  reduce compilation time of user apps if only we modify internal
  classes.
  - We do not install headers of external_package classes any more. They
  are used internally and not exposed to the end user.
  - qpOASES: compilation of examples is removed.
* Windows support of master: string to char * and no "or"/"and" keywords
* Updated Travis-CI; now building on OSX as well
* Fixed makefile for HPMPC based CGT OCP solvers
* Updated generated Simulink interface; added support for qpDUNES...
  ... based CGT OCP solvers.
* typo in MEX function
* no extra input to integrate function for the backward seed anymore
* Added indicator for linear terms in the objective.
* Merge branch 'master' of github.com:mvukov/acado
* Merge branch 'master' of github.com:acado/acado
* Working on linear terms in the CN2 solver, NMPC case only, for now.
* Fixed base class, CGT NLP solver, for linear term weights
* Fixed a bug when exporting zero statements, aka X = 0
* Simplified building of examples...
  ... disabled building of examples as a separate project.
* Refactored tunneling of LSQ linear terms from OCP specs to CGT.
* Updated the HPMPC interface
* Fixing a bug with exporting functions with OnlineData inputs
* Accelerated qpOASES QProblem class...
  ... In particular, I optimized the method
  QProblem::setupCholeskyDecompositionProjected, which was quite
  inefficiently coded -- bottleneck for a bit larger cases with not so
  many constraints. This should be tested if it really pays off for really
  small problems.
  For an equ. constrained QP with nv = 183 and nc = 9 a speedup
  of cca 42% was observed.
* discovered a strange bug to be fixed in model_data class
* removed weird behaviour with acado.Equals in DifferentialEquation for MATLAB interface to C++ translation
* update of the templates in ACADO's MATLAB interface
* use of timer tic/toc in integrate MEX function
* Fixed a bug in FunctionEvaluationTree method isConstant
* Error regarding cross-terms is modified to warning...
  ... since it return false positives sometimes...
* merge from Milan's master
* CMake typos
* Merge branch 'master' of github.com:acado/acado
  Conflicts:
  src/code_generation/export_gauss_newton_cn2.cpp
* Fixed makefiles for qpDUENS based OCP solvers
* default print level of qpDUNES set to 0
* Added makefile for the qpDUNES based solver
* Working on the MHE expansion in the CN2 solver
* Added a possibility for external factorization of the Hessian in CN3...
  ... based OCP solver
* Added MEX compilation script for the qpDUNES based solvers.
* wrote an interface for the new version of qpDUNES
* Working on the CN2 solver for the (partial) condensing case.
* Cleaning the CN2 solver
* fixed multipliers expansion for new N2 condensing
* default print level of qpDUNES set to 0
* Merge branch 'master' of github.com:mvukov/acado
* Fixed registration of the QpDunes based OCP solver.
* fix of the loading performance for symbolic expressions
* Merge branch 'master' of github.com:mvukov/acado
* Working on the HPMPC interface
* Fixed the examples in the CGT folder.
* bug fix related to online data and IRK methods
* unused variables in bioreactor example
* removed files for IRK with adjoint sensitivity propagation, since there is currently no satisfactory implementation possible for this
* Fixed export of the pointer for OnlineData in FunctionEval..Tree class
* add cpplint to the build system
  This commit adds cpplint.py, the google C++ stylechecker script.
  It also adds a CppLint.cmake module which provides the "add_style_check_target"
  cmake function. I used this to add a "lint" target for all ACADO_SOURCES.
  Type "make lint" to run the linter.
* added OCPexport::setName to the MATLAB interface in the stable branch `#101 <https://github.com/LCAS/acado/issues/101>`_
* Fixed the Simulink interface for the new OnlineData stuff
* Fixed the mex interfaces for the new OnlineData stuff
* Removed kinda obsolete CPU flags stuff for CMake
* Simplified the build system
* Added hasHessian flag in the QProblemB of the embedded qpOASES
* Cleaned a bit the CMake scripts
* Added c++11 support in a so-so clean way.
  TODO Enforce min compiler version to e.g. gcc 4.6 and/or clang 3.0.
* script to run all MATLAB examples of ACADO with error report
* removed pause command in crane from MATLAB example
* First steps towards unit tests
* First steps towards unit tests
* merged stable bug fix into master
* fixed bug related to online data and projections
* added a warning message for new N2 condensing related to state bounds
* fixed two bugs related to mexinputs of matlab interface
* Interfaced the GF's HPMPC solver
* Cleaned the ExportNlpSolver class a bit and added HPMPC type
* fixed forward_over_backward propagation
* Cleaned Hessian computation in the N^3 condensing.
* Revived cross-coupling block calculation simplifications.
* Added getSparsityPattern() to Expression class, see `#97 <https://github.com/LCAS/acado/issues/97>`_
* Added S-stage-Hessian terms in the N^2 condensing.
* Removed simplification of S1 in the CGT...
  ... cause I dunno correct way to calculate sparsity of an expression.
  See `#97 <https://github.com/LCAS/acado/issues/97>`_.
* Fixing/simplifying objective eval. in N2 generated solver.
* Added cross term var. setup in NLP solver export, case of external AD
* Added computation of the cross term weighting part to the N2 solver...
  ... plus simplified a lot the code for obj evaluation.
* Added computation of the cross-terms in the NLP export class...
  + added checks (disabling) to the corr. OCP solvers.
  + added isDiagonal() method to ExportVariable -- to do simplifications
* finished N2 condensing for exact Hessians
* Fixed an indexing bug in the CN2 condensing found by @rienq
* Fixing MEX iface for the OCP CGT solver
* enhanced integrator MEX interface regarding three-sweeps-propagation
* Print input array dimensions in the RT integrator declaration
* Addendum to the previous commit -- related to the common header in sim
* Removed dependency in the integrator common header on aux fcns file
* first implementation of N2 condensing with general Weighting matrices + expansion of lagrange multipliers, potentially for exact Hessians
* Updated CN2*, FORCES and qpDUNES based OCP solvers, see `#84 <https://github.com/LCAS/acado/issues/84>`_
* CN3 solver update, see `#84 <https://github.com/LCAS/acado/issues/84>`_
* Working on `#84 <https://github.com/LCAS/acado/issues/84>`_
* cleaned up power operators
* simplified AD operators for addition and subtraction
* solved bug in IRK methods caused by change in backward differentiation
* cleanup from initDerivative stuff
* fixed bug in symmetricAD operator of power
* implementation of proper propagation of initDerivative calls + renaming of ADsymmetric
* elimination of trivial tree projections
* turn nontrivial expressions automatically into an intermediate state
* optimization of power (but it still has the same issue as quotient)
* solved memory leaks in power and quotient operator
* implemented a myLogarithm feature
* implemented a myPower feature
* simplified Addition class
* simplified Product class
* improvement of quotient operator in AD symbolics (not optimal yet)
* added mySubract feature to operator class
* unified the different ways of creating a tree_projection via operator= (2)
* unified the different ways of creating a tree_projection via operator=
* fixed memory leak in unary_operator
* solved bug regarding to recent AD improvements
* optimization of unary operators in AD symbolics in terms of exporting expressions and their derivatives: much better reuse of auxiliary variables
* typo in export_nlp_solver.cpp
* ignore txt files in basic_data_structures examples folder
* derivative member of unary operator
* Merge branch 'master' of github.com:borishouska/acado
* start of implementation of 'new' CN2 condensing
* changed example
* added intermediate states in operator construction
* removed warning from symmetricAD example
* Merge branch 'master' of github.com:mvukov/acado
* typo in export_nlp_solver.cpp
* Fixed the issue reported by @rienq related to general w. matrices...
  ... when using the N^2 solver.
* Small fix to the objective eval in the N2 solver
* merge of Milan
* Merge branch 'master' of github.com:rienq/acado
  Conflicts:
  src/symbolic_expression/expression.cpp
* added example for debugging
* fixed a minor bug in new symmetric AD feature
* update of the integrator mex interface for the 3 sweeps propagation
* new 3 sweep propagation based on new symmetric AD feature
* clean-up of ADsymmetric routine
* minor cleanup of expression.cpp update
* update of symmetricAD example
* improved symmetricAD tool 2
* improved symmetricAD tool
* update of symmetricAD
* update of symmetricAD
* started development of extensions to the CN2 condensing: S-terms and expansion of lagrange multipliers
* Fixes `#91 <https://github.com/LCAS/acado/issues/91>`_
* Variable bound values in OCPexport with FORCES interface
* minor bug regarding forces interface: call to solve function
* corrected doc of ubAValues
* fixed minor bug when having variable state bounds in N2 condensing
* fixed minor bug with variable control bounds in both standard condensing and N2 condensing
* fixed minor bug with variable control bounds in both standard condensing and N2 condensing
* fixed minor bug with variable control bounds in both standard condensing and N2 condensing
* fixed minor bug with variable control bounds in both standard condensing and N2 condensing
* fixed minor bug when having variable state bounds in N2 condensing
* corrected doc of ubAValues
* merge with Boris
* modified function.cpp
* removed the dimension argument from function 'returnLowerTriangular'
* moved functionality of clearing all static counters, not limited to MATLAB interface anymore
* minor reformatting
* minor reformatting
* fixed warning in three-sweeps integrator
* fixed warning in function.cpp
* Merge branch 'master' of github.com:mvukov/acado
* resolved merge conflicts
* Merge branch 'master' of github.com:rienq/acado into stable
  Conflicts:
  examples/basic_data_structures/function/symbolic_differentiation3.cpp
  external_packages/src/acado_gnuplot/gnuplot_window.cpp
  include/acado/utils/acado_types.hpp
  src/symbolic_operator/projection.cpp
* added symmetric AD functionality, fixed ADbackward, enabled stacking of variables
* added custom functionionality for the new three-sweeps-propagation approach to make it at least competitive with forward-over-backward, currently lacking specific AD functionality for the operators involved
* improved forward-over-backward second order sensitivity propagation in ERK methods using the new AD functionality
* improved forward sensitivity propagation in ERK methods using the new AD functionality
* added AD support for forward and backward derivatives with matrix seeds
* improved speed of ERK methods forward sensitivity propagation
* Tuning the N2_FACT... solver
* Cleaning the CN2_FACT... solver.
* Fixing a bug in return value from Cholesky decomposition.
* Updated the CN2_FACT... solver ...
  - Optimized export of the condensing and factorization routines for
  long horizons.
* Optimized export of Cholesky and corr. solver routines...
  ... used for N^2 factorization.
* Fixed printing of ExportVariables of type INT
* interfaced Cholesky of the condensed Hessian ...
  ... to qpOASES based OCP solvers
* Added options for decomposition of condensed Hessian.
* Added API for tunneling the ext. Cholesky decomposition to qpOASES
* Working towards support for external Hessian Cholesky decomposition.
* Added "hasCholesky" flag to the qpOASES embedded
* Merged stable, 855a125
* Merge branch 'stable' of github.com:tibnor/acado into tibnor-stable
* Fixed a bug related to export of RT integrators.
  @rienq please take a look
* Implemented the N^2 condensed Hessian factorization, nx^3 free...
  ... for the CN2_FACT... solver.
* finished implementation of sensitivity propagation techniques for ERK methods
* finished implementation of FORWARD over BACKWARD sensitivity propagation for ERK methods with an update of the MEX interface
* #include <unistd.h> is only included if not on WIN32 (which does not have unistd.h)
* added a FORWARD_OVER_BACKWARD propagation feature for ERK methods in code generation
* updated all the code generation MATLAB examples according to the new integrator MEX interface
* finished code generation of ERK methods with adjoint sensitivity propagation
* improved the ACADO integrators MEX interface
* improved the ACADO integrators MEX interface
* support for adjoint sensitivity propagation in ERK methods
* automatic detection of symmetry in Butcher table of RK methods
* automatic detection of symmetry in Butcher table of RK methods
* crane NMPC example in Matlab interface fixed
* Merge branch 'master' of github.com:mvukov/acado
* Fixed a typo
* Merge branch 'master' of github.com:mvukov/acado
* Fixed solver initialization of CGT solvers...
  ... We only initialize workspace struct to zero. Everything else, aka
  variables init is up to the user.
* update of IntegratorExport with the new error code + improved check of linear subsystem
* added an option for invalid function definitions in a linear output subsystem
* minor fix in sim_export for the case of extra outputs
* .gitignore not needed anymore
* updated the Matlab examples, accuracy of integrators is now computed by exporting two different methods
* No longer support for a separate interface to the model right-hand side because there are currently more exception cases than regular cases, creating problems for long-term maintainance of the code
* Merge branch 'master' of github.com:mvukov/acado
* minor bug fix in the new robot NMPC example
* new simple but illustrative NMPC example in Matlab interface based on the FMTC robot
* reduced the interface functions for setDimensions to a more compact and clear set + update of the Matlab interface
* fix in fullRhs, but currently an error to be fixed in case of (semi-) implicit model formulations
* Updated year info in acado_utils.cpp
* Merged stable, 2b91458
* Fixed `#83 <https://github.com/LCAS/acado/issues/83>`_
* Updated licensing info
* Working on CN2_FACT... solver. Factorization works.
* Hokay, CN2_FACT... solver code is taking some shape...
  ... but it does not work. First block row of the condensed Hessian is
  correct, but the update of the Q1 block seems to be wrong.
* Added solve fcn to the Cholesky solver.
* Added Cholesky based linear solver...
  ... which is gonna be used in the new condensing implementation.
  So far, only the in-place Cholesky has been implemented.
  + A small fix in it's base class
* Working on CN2_FACT solver...
  Added description.
* Merge branch 'master' of github.com:acado/acado
* parallel compilation of ACADO in Matlab interface
* Working on the CN2_FACT... solver
  Forgot to commit a change to the header file.
* Working on the CN2_FACT... solver
  Both ctrl and state constraints should work now.
* Fixing CN2_FACT... solver. Input constrained case seems to work now.
* OKAY, fixed the CN2_FACT... algorithm
  Forming of condensed Hessian should be fixed now.
* parallelization in compilation procedure of ACADO with Matlab interface
* renaming of printToFile to print
* update of gitignore for Matlab interface examples
* Fixed indexing issues in CN2_FACT... solver related to the cond. Hess.
* Fixed an indexing bug in the CN2_FACT...
* fix: use of DVector instead of Vector
* BMatrix fix in Matlab interface
* update crane example
* BMatrix instead of ExportVariable in OCPExport
* no setTimingCalls for OCPexport
* fix for the setDimensions in case of externally defined model
* fix of two examples in code_generation/simulation
* SIMexport tutorial to be added
* bug fix for online data
* fix for externally defined output functions
* update of externModel example
* exportAcadoFunction instead of remembering names of externally defined functions
* Working on CN2_FACTORIZATION solver
* Cleaning the condensing based solvers, making code a bit more readable
* Working on CN2_FACTORIZATION solver
* Fixed a minor bug when exporting argument lists.
* Working on the exported OCP solvers:
  - moved xBoundIdx array from the main class to derived, because this
  is something condensing specific;
  - cleaned a few minor thins and renamed some variables.
* Added the CN2_FACTORIZATION solver to the user interface
* Added files for a CN2 solver with factorization routine.
  (Copied files from the CN2 implementation).
* Merge branch 'stable' of github.com:acado/acado
* Updated project version info
* update from Parameter to OnlineData
* update of MEX interfaces for SIMexport integrators
* added OnlineData class to Matlab interface
* update of MEX interfaces for SIMexport integrators
* fix of SIMexport integrators for Linux
* update regarding new templates for MATLAB interface
* exportCommonHeader for SIMexport
* cleanup of SIMExport
* exportAuxiliarySimFunctions
* added a few templates for SIMexport
* minor update integrate mex function
* .gitignore files not necessary anymore
* Fixed a mem leak in the symbolic core.
* removed acadoPrintf in getCPPbody
* minor update of the mex interfaces for the integrators
* replaced readFromFile with the appropriate read commands
* setTimingSteps instead of setTimingCalls
* Merge branch 'master' of github.com:acado/acado
* Merge branch 'master' of github.com:acado/acado
* update Matlab interface with new eigen3 library operators
* updated templates Matlab interface
* removed modeling tools from Joris
* Merge pull request `#74 <https://github.com/LCAS/acado/issues/74>`_ from ThomasBesselmann/patch-4
  Declare mexInput variables in FB to avoid erros due to their use before ...
* Merge pull request `#73 <https://github.com/LCAS/acado/issues/73>`_ from ThomasBesselmann/patch-3
  Declare mexInput variables in FB to avoid erros due to their use before ...
* Merge pull request `#72 <https://github.com/LCAS/acado/issues/72>`_ from ThomasBesselmann/patch-2
  Declare mexInput variables in FB to avoid erros due to their use before ...
* include eigen3 library in the MATLAB interface build
* Fixed formatting in ExportVariableInternal
* Fixed printing of integer typed matrices.
* Fixed export of MVM and MMM, case when loops are not unrolled.
* Fixed main CMake file so that we can use Eigen3 from external projects
* Merge branch 'master' of github.com:mvukov/acado into stlification
* Minor fix in the CGT closed loop Simulink example
* Updated generated makefiles to use ccache if installed
* Fixed the Simulink CGT example
* Cleaned header inclusion in the CGT + ...
  ... registration of the exported NLP solvers is decoupled from the
  user interface now.
* Merged master and resolved conflicts...
* Cleaning the CGT
  - Minor cleanup of some files
  - Cleaned the export of MMM routines, in general
  ExportArithmeticStatement should be cleaner now.
  - Main CGT header cleaned so that it includes mostly
  user interface classes.
* Added a convenient way to enter OCP constraints, for coupled interfaces
* no error for discretized differential equations anymore related to code generation, although the correct integration method should be chosen by the user
* Cleaned the qpOASES interface for the CGT OCP solvers.
* Working on `#80 <https://github.com/LCAS/acado/issues/80>`_. On-the-fly constraints are fully supported for...
  ... qpOASES based OCP solver. TODO Write documentation...
* Merge branch 'master' of github.com:mvukov/acado into stlification
* Added BitDeli badge info
* Merge pull request `#71 <https://github.com/LCAS/acado/issues/71>`_ from ThomasBesselmann/patch-1
  Added new condition to avoid problems with empty reference field
* Changed the way of handling of external fcns in the CGT...
  ... and fixed a bug in ExportAcadoFunction
  (which can be "external" btw)
* A small fix in the symbolic core for the VT_TIME variable
* Merge branch 'master' of github.com:mvukov/acado into stlification
* Updated handling of external sym evaluation fcns in the CGT.
* Added "external" functionality to ExportAcadoFunction
* ASSERT calls abort(), again
* Changed the way how we initialize the solver.
* preparationStep returns status of the integrator.
* Updated CGT pendulum DAE example.
* Improved export of export of extern objective functions...
  ... for condensing based OCPs. This should be further improved for all
  OCP solvers we use.
* Improved efficiency in ExportFunctionDeclaration and...
  ... removed cloneFunction from ExportFunction.
* Fixed the dummy file in the CGT so that we can compile it by
  default in the MHE case, too.
* Some minor fixes for the CGT...
* Merge branch 'master' of github.com:acado/acado into stlification
* Yeah, the new Simulink closed loop example patch
* Hopefully the last commit to the Simulink closed loop example for today...
* Merge branch 'master' of github.com:acado/acado into stlification
* Resolved conflict in the Simulinke example
* Improved documentation for the Simulink closed loop example, as well as few minor thingies
* Improved documentation for the Simulink closed loop example, as well as few minor thingies
* Merge branch 'master' of github.com:acado/acado into stlification
* Improved documentation for the Simulink closed loop example, as well as few minor thingies
* Merge branch 'master' of github.com:acado/acado into stlification
* Fixed a minor bug in the crane closed loop Simulink example
* Merging 453dd9ec191fe87048ff2ad42627506e2a8035a0
* Merge branch 'master' of github.com:acado/acado
* Merge pull request `#78 <https://github.com/LCAS/acado/issues/78>`_ from ferreau/master
  Update export_nlp_solver.cpp
* Fixed `#76 <https://github.com/LCAS/acado/issues/76>`_
* Fixed `#77 <https://github.com/LCAS/acado/issues/77>`_
* Update export_nlp_solver.cpp
* Declare mexInput variables in FB to avoid erros due to their use before declaration
* Declare mexInput variables in FB to avoid erros due to their use before declaration
* Declare mexInput variables in FB to avoid erros due to their use before declaration
* Added new condition to avoid problems with empty reference field
* Explicitly disabled usage of Parameter class in the OCP solvers...
  ... as well as in the integrators. Users should use the OnlineData
  class.
* Updated templates: Parameter -> OnlineData
* CGT: Parameter -> Online data, to the rest of the CGT...
  ... testing tomorrow.
* CGT integrators: Parameter -> OnlineData
* Part of the CGT example does not work:
  - @rienq please take a look at this. I left some comments in the
  example' source.
* Tunneling of OnlineData structure in progress:
  - Had to heavily mod model_data since there were fcn overloading
  problems.
* Cleaning export of ACADO function
* Tunneling of OnlineData to the CGT
* fixed export-to-c example
* Fixed a bug in SymbolicIndexList
* Cleaned the Output symbolic class.
* Deleted old variable type classes
* Refactored a bit the symbolic core. Using CRTP for variable types.
* Added VT_ONLINE_DATA that is going to be used in the CGT
* math.h -> cmath in utils
* Fixed a warning in the export of an acado fcn.
* Enabled compilation of all CGT exampled.
* Cleaning CGT -- how we tunnel module name and export folder name.
  Those are the options now, as they were supposed to be from the start.
* Fixed options functionality. String-valued options work now.
* Building the my_examples folder again
* ExportNlpSolver: added more rigorous checks for the objective fcn
* Added isConstant() to the Function class
* Fixed CGT simulation examples
* Fixed minor bugs in the CGT
* Finished tunneling of weighting matrices sparsity patterns.
  Tested only with getting_started example.
* Tunneling weighting matrices sparsity pattern to the CGT
* Major rework in ACADO syntax:
  ---> ones, zeros and eye are template functions now.
  This slightly complicates the syntax, but makes it more general.
* Merging master, e9ded59
* Solved a serious bug in the CGT, see `#68 <https://github.com/LCAS/acado/issues/68>`_.
* Export of common header in the CGT is more automated now.
* ExportAlgorithm cleanup
* Cleaned ExportVariable.
  - removed some functions that are not gonna be used any more
  - cleaned some code. ExportVariable is not a friend of
  ExportVariableInternal any more.
* Fixed a few minor bugs. CGT works now in a basic mode...
  ... with "given" weighting matrices.
* Fixed a bug in export file.
* Properly coded casting from ExportIndex to ExportArgument...
  ... via operator ExportArgument() in ExportIndex.
* Removed a hack in ExportFunction
  retVal is now pure ExportVariable
* Simplification of ostream formatting for function export
* Fixing bugs in export of an acado function, cgt interface
* Cleaning export variable, internal
* Fixing export of acado symbolic functions.
* Introduced ostream formatter.
* CGT is enabled in the main CMake sctipt + ...
  - CGT is not any mode in the optimal control header but in the
  main acado_toolkit.hpp.
* Fixed some CGT examples + ...
  closed loop examples are disabled for the moment.
* Fixed a small bug, 0 -> "", in OCP export
* Fixed internal of export variable
* Cleaning and fixing ExportIndex class
* Fixing ExportNLPSolver for the new API
* Fixed a stupid big in ExportFunction
  related to stream-to-stream printing...
* Fixing objective and constraint classes
  - Objective classes prepared for the new matrix/vector API.
* Cleaning OCP and NLP classes
* Removed unnecesary files
* CGT conforms the new m/v API and compiles, though does not work.
* Added another isFinite function...
* Added printing more info in case Hessian is ill formed.
* Fixed ocp/lsq_term example
* Added condition number checking of condensed Hessian, see `#49 <https://github.com/LCAS/acado/issues/49>`_.
* Added condition number calculation for square matrices based on SVD.
* ACADO optimal control and simulation classes work, BUT:
  - I had to disable BDF integrator code
  - this means that BDF int. cannot be used at the moment
* Fixed OCP and Simulation classes
* Fixed qpOASES interface
* Fixed Matrix class, ctor and P(S)D checking
* correct crane NMPC example in MATLAB
* Examples for ACADO integrators scope compile
* ACADO integrators refactored.
* correct crane NMPC example in MATLAB
* BDF does not work ATM.
  Have to figure out how to use QR decomposition from Eigen here
* Algorithmic base fixed to the new API
* Symbolics fixed to the new API
* VariablesGrid, operator DMatrix()
* Grids, OK
* Matrix-vector back-compatibility
* VectorspaceElement -> DVector
* Matrix -> DMatrix, Vector -> DVector, project-wise
* OK, reverted the matrix-vector classes and made them almost...
  ... compatible with the old API.
* Polishing the matrix-vector class.
* Fixing bugs in the vector class
* Added mv tools
* Building the examples by default again
* Builing only matrix-vector examples for now...
* Refactored matrix-vector classes to be Eigen3 compatible
  + cleaned utils file.
* Added Eigen3 to external packages…
  … and removed old Matrix-Vector stuff
* Block matrix class storage is not based on STL
  TODO It might be more efficient to do 1D storage instead of 2D as it is
  now...
* Cleaning matrix and vector classes
* std::vector storage for Matrix like classes.
* Cleaned boolean type in the CGT
  Now we use standard C++ boolean type ;)
* Updated licensing info for pip files
* Updated lic updating: update ipp files, too
* Merge branch 'master' of github.com:acado/acado into stlification
* Upgrading project version to 1.2.0beta
* CGT: timing functionality moved from ExportModule to SIMexport
* CGT integrators cleaned and fixed
* Small fix for export of arithmetic statements
* CGT linear solvers refactored
* STLification of the CGT started :D
* Added a function for "to-string" conversions.
* CGT: Stream -> std::ostream, String -> std::string
* Completed adding std::string as options in the Options class.
* Options eye-candy and formatting improved
* Refactoring options classes
* fix for Windows MATLAB interface
* fixed iteration printiing in the scp method class
* Fixed Gnuplot interface
* Updated example
* Debugging logging functionality
* Updated input files for examples.
* Debugging logging functionality
* Removed CGT includes from OC header
  Probably temporarily.
* Added ACADO_WITH_TESTING preproc. def...
  And modified message handling. In testing mode, an app should fail
  on all errors.
* Updated some examples to the new code... Now everything complies
  smoothly. Some examples fail, but this will be debugged later...
* Cleaned OC and Simulation classes..
  It was not possible to link OC classes into a lib w/o Simulation
  classes; this is why this huge commit is created. However, not so many
  changes have been performed...
  Important: the OCP class does not depend any more on ExportVariable,
  Matrix class is used instead, which has de be refactored to include
  sparsity patterns, e.g. simple vector< bool > array and move this
  functionality from ExportVariable.
  So far, everything except CGT, which should sit atop the toolkit,
  compiles.
* Fixed Logging class...
  setAll functions were removed -- as I removed LogCollection class...
* Merge branch 'master' of github.com:acado/acado into stlification
* Cleaning and fixing Optimal Control type classes...
  - So far everything except ocp and optimization_algorithm folders
  compiles
  - Fixed interface to qpOASES
* Patched qpOASES -- related to definition of the BooleanType
* Moved model_container and model_data to ocp folder(s)
  In order to cut deps between off-line and CGT ACADO, it is necessary
  to move those 2 classes to another folder. OCP class is the one that
  inherits from model_container in offline ACADO, thus I chose to move
  those two guys over there.
* Cleaned integrator examples...
  ... as well as integration_algorithm examples -- but I cannot compile
  them so far as they depend on optimal contol set of classes.
* Updated examples for new changes:
  - basic_data_structures folder
* Cleaned and debugged symbolic core
  - Returned some constructors I previously removed
  - Improved printing functionality
* Updated matrix-vector classes -- printing functionality
  + Added a few streaming operators (template functions) to utils
* close Issue `#65 <https://github.com/LCAS/acado/issues/65>`_
* Small update to the Gnuplot interface...
* Cleaned Gnuplot interface class.
* Minor update to MatrixVariblesGrid
  Added a not-so-clever sprint function to be able to finish refactoring
  of the gnuplot interface.
* Cleaned elipsoidal interarator classes
* Cleaned (offline) integrator classes
* removed a few compiler flags on Mac systems
* Cleaned the user interface classes
* only measurement points should be provided by the user
* Merge branch 'master' of github.com:acado/acado
* updated examples with new interface for continuous output
* implemented support for arbitrary measurement grids
* Further STLification of symbolics and function classes.
* Small update in the matrix class
* Turned of compilation of examples for a while...
* Cleaned grid classes...
  ... and
  - Enabled compilation of the sparse solver classes, cleaned them as well
* Polished matrix-vector classes
  ... added input streaming ops
* Added input streaming ops for vector and vector<vector>
* Cleaned and modified the matrix-vector classes
* Cleaned and modified the utilities
* Cleaned and modified the utilities
* Doxygen automatic upload works; changed build rules so that the doc is uploaded only when we push to the _stable\_ branch
* Merge branch 'master' of github.com:acado/acado
* Fixing Travis-CI scripts
* removed the OS SYSTEM option in SIMexport
* updated MATLAB examples, no OS option anymore
* Boring... fixing the apidoc upload script
* Added version info to the zip
* chmod +x on travis_before_install
* Polishing Travis-CI scripts
* Updated doxygen mainpage
* Fixing the Travis-CI stuff
* Added script for automatic update of documentation
* Documented deploy_code.sh
* Renamed the script for publishing of the apidoc
* Modified doxygen conf; noew creates additional folders to speed up browsing
* Removed wiki from the doxygen build; this is still under dev and for now we will stick with the SF based website
* Cleaned the code-deploy script
* Working on `#62 <https://github.com/LCAS/acado/issues/62>`_
* Fixing the travis-ci code deployment script...
* Fixing the travis-ci code deployment script...
* Fixing the paths in the travis-ci script...
* Added deployment of the source code
* With Cygwin we build static libs only
* Merge branch 'master' of github.com:acado/acado
* made acado compile on cygwin
* Merge branch 'master' of github.com:acado/acado
* Updated export of symbolic functions...
  - Names are shorter now, this results in a bit smaller file sizes...
  of the exported code.
* better support for external models in MATLAB codegen make files
* update .gitignore files to cleanup output of git status
* small update to MATLAB example file
* removed automatic build script
* updated code generation examples in ACADO MATLAB interface
* update templates in MATLAB interface
* removed all files MATLAB interface for code generation
* fixed OCPexport in ACADO MATLAB interface, removed automatic build system which is now replaced by auto generated Makefiles
* added 2 new templates to compile integrators
* Fixed documentation generation of exported code
  - Minor formatting in ExportFunction, declaration part
  - .... and in the export of ACADO symbolics
* reverted the changes in SIMexport partly
* removed one warning related to unused variable
* small update of SIMexport file names
* only declare user accessible functions in acado header file
* Merge branch 'master' of github.com:mvukov/acado
* Merge branch 'master' of github.com:acado/acado
* Updated MEX interface for CGT OCP solver
  - Added support for covariance output (if enabled)
  - Added support for algebraic variables.
* fixed issue with full_rhs in case of 3-stage model format
* added automatic creation of export folders in SIMexport
* updated ACADO from MATLAB code generation simulation examples + added a quadcopter example to illustrate 3-stage format
* updated existing SIMexport ACADO from matlab examples
* update external Pendulum model
* fixed the build problem in ACADO MATLAB interface
* updated C++ SIMexport examples
* updated C++ SIMexport examples
* Removed some lightly unnecessary asserts
  - In the Householder QP decomposition, since `#46 <https://github.com/LCAS/acado/issues/46>`_ is solved
  - In the ExportAcadoFunction, because it is giving me more headache
  than helping me debug the code. There is a comment and todo there now.
* Initialize function return a status value
  + by default, it is 0.
  + qpDUNES interface init function, `initializeQpDunes` returns status
  via main init function, `initialize`.
* Setting the name of exported function call is fixed.
* Fixed typos in CGT test files.
* Added documentation for CGT arrival cost calculation.
* Fixed some dev examples, we can be compile them
  … now. Most probably they still don't work...
* dev and internal -> Now are options..
  .. instead of cached strings
* Added a closed loop example in Simulink…
  … for the simple crane.
  NOTE: So far it works in Normal mode, but not in
  Accelerated mode - there are certain compilation
  problems to be solved.
* Simulink MEX make script for CGT updated
  … working on full customization...
* Renamed the KUL crane MHE example
* Fixed and upgraded customization of make script
  … for Simulink interface.
* Added customization of exported aux functions
* Fixed a minor bug in ExportModule
  - custom file names work now.
* Added a definition for the qpOASES embedded…
  … main folder.
* Simplified the CGT getting started example
* Udated documentation
  - Added the new logo
  - Added CGT getting_started example
  - Updated wiki
  - Removed tree view from oxygen
  - Added citing page in wiki
  - Updated wiki pages here and there :)
* CGT: weighting matrices names changed:
  - S -> W, generated in acadoVariables
  - SN -> WN, generated in acadoVariables
  This is deliberately done because Simulink coder
  is not happy with structure fields with name "S".
  This is not backwards compatible and it is going
  to break old codes.
  Generator changes are only in ExportNLPSolver
  class. Examples and Matlab+Simulink interfaces
  are updated accordingly.
* Merge branch 'pre120beta' of github.com:mvukov/acado into pre120beta
* Added missing files in getting_started CGT example
* Link rt library in ACADO_GENERATE_COMPILE CMake macro
* Fixed bug in initialization and shifting codes in case when DAE is used
* Updated and simplified code generation of examples
  … in CGT
  - Added macro for generation and compilation of
  exported code, see cmake/UseACADO.cmake
  - Fixed crane mhe and penudulum dae examples
  - Adopted the build system a bit.
* Removed the test file for the getting_started
  … close loop example in CGT.
  I have added MATLAB and Simulink tests plus
  the dummy file actually works with this one ;).
* Removed the crane example…
  Since it is the same as the getting started one...
* Added S-function example for the CGT getting_started
* Added MATLAB example for CGT getting started example
* Updated readme.md
* Updated generation of qpOASES embedded interface
  See issue `#52 <https://github.com/LCAS/acado/issues/52>`_
* Updating CGT examples
  TODO Build rulez for tests
* Added test files for some example
* Added two more examples
  … And fixed the .gitignore in examples folder.
* Renamed examples folder for MPC and MHE
* Eye candy update for CGT NMPC example
* Fixed the issues regarding the configuration and export of templates...
  ... in CGT. Now this should work with `make install` as well. Needs to
  be tested, though.
* Fixing a bug...
* Removed support for the CVXGEN in the CG tool.
* Rename ExportODEfunction to ExportAcadoFunction
* Fixed small issue with CGT templates and the build system
* Updated NMPC CodeGen examples…
  … according to the new CGT
* Small fix in the main code-gen include file
* Cleaned the nmpc code-gen examples folder
* Added the new code generation suite
* Merge branch 'pre120beta' of https://github.com/mvukov/acado into pre120beta
* Removed exported RTI scheme class. See `#50 <https://github.com/LCAS/acado/issues/50>`_
* Removed exported RTI scheme class. See `#50 <https://github.com/LCAS/acado/issues/50>`_
* Cleaned export of acado functions.
* Small fixes in the utilities
  - Update lic info
  - destructor of returnValue: abort -> exit. This is less aggressive and
  scary I would say. However, there is still the memory leak. See `#51 <https://github.com/LCAS/acado/issues/51>`_
* Do not export function call for an empty function
* Fixed some bugs with ASSERTS in the Debug mode.
* Merge branch 'master' of github.com:mvukov/acado into pre120beta
* Minor preparation for the new Simulink interface in CGT
* Updated and fixed a small glitch in the license
* Merge branch 'master' of git://github.com/rienq/acado into pre120beta
* Fixed main CGT header
* Updated CGT templates
* Cleaned the OCP class
* Cleaning of the CGT
  - Removed some old files, mainly the OCP solver
  - Removed some rarely used classes
  - Removed classes which are going to be deprecated
  - Patched some classes so that we can compile ACADO
* Updated build system
  - Removed lic info
  - Disabled building of the code gen examples
  (temporarily)
* Updated licensing info
* Added files for updating of the license info
* Updated main gitignore file
* Small update
* Updated algorithm factory functionality
  - Moved typedef for integrator factory to its base class
  - Added some documentation
* Extending the export of templated files
* removed some warnings regarding the move of diffsDim and inputDim in export of integrators
* Updated readme
* commit should solve issue `#46 <https://github.com/LCAS/acado/issues/46>`_
* Merge branch 'master' of github.com:mvukov/acado
* external model support for explicit integrators (see issue `#47 <https://github.com/LCAS/acado/issues/47>`_ on GitHub)
* Minor fix in export of argument lists...
  ... that made possible to have function argument of ExportVariables of
  types STATIC_CONST\_{REAL, INT}
* Updated main README file
* Simplified export of expressions like: Var = zeros(X, Y)
* Added isSubMatrix to ExportVariable
* Merge branch 'master' of github.com:francesco-romano/acado into francesco-romano-master
* Updated ExportFunctionCall
* Working on `#38 <https://github.com/LCAS/acado/issues/38>`_
* Merge branch 'master' of github.com:mvukov/acado
* Updated Householder QR
  - Moved back-solve code before the actual solver fcn.
* added the -std=c99 as a C flag for compilation of ACADO exported code
* Updated Householder QR based solver and found a bug
  - The solver works for A with dim nRows >= nCols
  - Fixed a bug related to the case w/o reuse feature
  - Disabled export of the solver in case reuse it TRUE, until bugs are
  fixed
  - Added calculation of determinant, the solver return determinant of
  matrix R now.
* Generalized export of linear system solvers
  - This is initial commit for this work.
  - Idea is to implement custom lin. sys. solver with QR (at least), for
  cases m >= n;
  - Added customization for the number of backsolve steps, <= n.
* Fixing minor bug in ExportFunction
* Merge branch 'master' of https://github.com/mvukov/acado
* Added CMake script unit testing based on Boost unit testing framework
* Added streaming operator to the String class
* Updated exporting of functions:
  - Export(ODE)Function: improved mem. manageement. + cleaning
  - Export in Function class: empty functions are not being exported.
* Added a few streaming operators to ExportStatementBlock
* created AdjointIRKExport class
* minor cleanup regarding IRK sensitivities
* bug fix for right-hand side MEX function in Windows
* Merge branch 'master' of github.com:acado/acado
* fixed recently introduced bug in ModelContainer
* Merge branch 'master' of github.com:acado/acado
* small bug fix related to automatic MEX build script and Simulink exported interface
* Added examples/my_examples
* Merge branch 'master' of https://github.com/mvukov/acado
* Small fix in the OCP class...
  ... so that it does not report an error when number of intervals in
  the ctor is set to 0 -- this would return a warning when an NLP is
  defined.
* Updated examples
  ... in a way to really return error codes when an error happens. This
  way we can easily use a new testing feature from the build system.
* Updated .travis.yml
* Merge branch 'master' of github.com:mvukov/acado
* Added exportFolderName field to the ExportModule class...
* Updated ExportModule class
  - removed setCommonHeaderName() function. setName() of the same class
  will update the commo header name, if needed. This is on the TODO list.
* Added addition operator to the String class
* Polishing ExportModule UI structure...
  - Added field <name>, in order to be able to prefix the exported files.
  - Minor cleaning in the mpc_export class.
* Added acadoCreateFolder function.
  ... Works on UNIX, should be tested on Windows+MSVC.
* Fixed assertions...
* Build system updated
  - When we are building "test" target for unit tests,
  __NO_PLOTTING_\_ def is used to prevent plotting.
  Thus, ACADO_WITH_TESTING should be used with care.
  - BTW: unit tests can be enabled from command
  line with cake:
  cmake -DACADO_WITH_TESTING=ON ..
  - Multi-objective examples are not in unit tests -
  contact Filip to see whether he would like to
  maintain this.
  - Minor polishing…
* Polished Gnuplot interface…
  - when __NO_PLOTTING_\_ def is defined, we are
  not plotting anything. This is introduced in the
  case we run unittest.
* Fixed ASSERT() macro
* Default name for interim. export variable changed
  … back to "acado_aux"
* Changed export folder path for kite carousel…
  … in code generation
* Moved default export to stdout.
* Sparse LU tutorial segfaults -> moved to dev.
* Merge branch 'master' of github.com:mvukov/acado
* Updated testing scripts
* Merge branch 'master' of github.com:mvukov/acado
* Fixed .travis.yml
* Fixed .travis.yml
* Updated Travis-CI script to run tests on examples after a successfull build
* Added automated testing functionality to example apps
* Prefixed with dev\_ examples which give segfaults
* Added variable initialization in UniformNoise constructor
* Merge branch 'master' of github.com:mvukov/acado
* Small bugfix...
* Working on decoupling standard ACADO and Code Generation Tool (CGT).
  Removed dependency of the standard ACADO on CGT while exporting ACADO
  symbolic functions, i.e. removed dependency on ExportVariable.
  Specific getter/setter functions are moved to the ExportODEFunction now.
  BTW, we should rename ExportODEFunction to ExportACADOFunction.
* Cleaning the ExportStatement infrastructure.
  Refactored derived classes in order to simplify coding of user classes.
  Main improvement is that certain (helper) functions return a reference
  to a given class.
* Working on performance issue while exporting "big" expressions.
  There is a performance issue while exporting big functions using
  ExportFunction. The issue is related to setVariableExportName function
  which is called recursively.
  Possible solution is just to call this function in TreeProjection
  class only for an argument of type Power_Int.
* Updated timestamp of the acado_utils file
* Replaced notifications of the exported integrator to the new style.
  The debug info can be enable in the user app with:
  Logger::instance().setLogLevel( LVL_DEBUG );
* Updated copyright notices.
* Merge branch 'master' of github.com:acado/acado
* Removed some warnings
* Merge branch 'isequal-uses-fabs-2' of github.com:roryyorke/acado into roryyorke-isequal-uses-fabs-2
* Merge branch 'debug-fixes' of github.com:roryyorke/acado into roryyorke-debug-fixes
* Removed a few varnings that Clang was constantly reporting...
* Merge branch 'master' of https://github.com/mvukov/acado
* Updated main doxygen file to compile the new markdown pages
* Added markdown wiki to the repo -- the same, a bit updated, content from the SF website
* Updated debugging tools section
* Removed old makefile and the mainpage -- doxygen related
* fixed bug related to parameter estimation in MATLAB interface
* Merge branch 'master' of github.com:mvukov/acado
* Update CompilerOptions.cmake
  Trying to remove unused-comparison with clang...
* Merge branch 'master' of github.com:acado/acado
* added the crane MPC example back to MATLAB interface examples
* Minor: whitespace fix.
* Bugfix: acadoIsEqual should use fabs() for rel vs abs decision.
  Code previously used maximum of signed arguments to decide whether to
  use relative or absolute tolerance check.  If this function is to also
  be used to compare negative numbers of large magnitude, the absolute
  value of its arguments should be used.
* WarningFix: remove always-true expression in assertion.
  The variable being checked for non-negativity is an unsigned int.
* Buildfix: Define __DEBUG_\_ for CMAKE_BUILD_TYPE Debug.
  This seems like the likely intent of the conditional compilation
  on__DEBUG_\_ in acado_debugging.hpp, etc.
  It might be better to take a leaf out of <assert.h>, and use NDEBUG
  instead.
* Bugfix: change isAccessedTransposed() to doAccessTransposed.
  This is a best-guess fix to allow compilation when __DEBUG_\_ is defined.
* Bugfix: allow compilation with __DEBUG_\_.
  The argument idx\_ is only used in an ASSERT; ASSERT, in turn, is a
  no-op unless __DEBUG_\_ is defined.  So, when __DEBUG_\_ is not defined,
  gcc would warn about an unused variable if the name is declared.
  Allow debug and warning-free non-debug compilation to occur by making
  argument name declaration conditional on __DEBUG_\_.
* Update .travis.yml
  Build code in debug configuration...
* Merge branch 'float-warnings' of github.com:roryyorke/acado into roryyorke-float-warnings
* Merge branch 'expression-print-bug' of github.com:roryyorke/acado into roryyorke-expression-print-bug
* Merge branch 'minor-warnings' of github.com:roryyorke/acado into roryyorke-minor-warnings
* Cleaned and extended the ExportVariable class
  ... + some minor cleaning in the ExportArith..Statement class.
  Added getElement method to access a single element of an ex. variable.
* Moved diag(.) of ExportVariable to it's own class definition file.
  -> Removed deps on ExportVariable.
* Cleaned and documented the OCP class
* Defined ExportVariable as forward declaration.
  Working on reducing deps on ExportVariable.
* Cleaned Gnuplot class
* minor bug fix related to models without control inputs or parameters
* Merge branch 'master' of github.com:acado/acado
* Fixed warning in the plotting module; Working on `#32 <https://github.com/LCAS/acado/issues/32>`_
* Fixed warnings in the Gnuplot interface
* Merge branch 'master' of github.com:acado/acado
* minor warning related to exported file integrator.c for ERK methods fixed `#32 <https://github.com/LCAS/acado/issues/32>`_
* Update .travis.yml
  Added notifications "hook" -- send an email in case of failure
* Update .travis.yml
  Added clang compiler to the test script
* WarningFix: prefixed local shadowing variable names with "ex".
* WarningFix: remove unused variable dummy, assign gcvt() return to third arg.
* WarningFix: remove unused variable bound2.
* WarningFix: remove unused variable cos_2phi.
* WarningFix: remove unnecessary const qualifier on return type.
* WarningFix: Remove unused variable nAC.
* WarningFix: remove unused variable obj (two instances).
* WarningFix: remove unused variable nFR and nFX.
* WarningFix: removed unused local variable nFR, nFX, nAC, and nIAC.
* WarningFix: Remove unused local variable m.
* Remove various minor warnings.
  Warnings are either unused argument (removed parameter name),
  unnecessary qualifier (removed const), or recommended braces for
  empty else clause (presumably when ASSERT is defined to be empty).
* Factor out isExactly* to a PrivateUtils file for reuse in BLASReplacement.cpp.
  As of this check-in there are no more -Wfloat-equals warnings.
* Remove all float-equality warnings in Matrices.cpp.
  The three types of equality check (to -1, 0, and +1) are replaced by
  inline functions with the float-comparison warnings turned off by a
  gcc pragma.
  It is still to be determined how to make this compatible with other
  compilers.
* Bugfix: handle no-element case when printing expression.
* Merge branch 'master' of github.com:acado/acado
* improved error message when exporting code from MATLAB interface
* fixed BUG with ERK methods because of overloaded function '*=' in Matrix class without a copy of the Matrix first
* fixed MPC MEX interface for Windows
* fix for timing results in MATLAB interface on Windows
* temporarily removed the crane demo from the MATLAB interface examples folder for the optimal control course in Stuttgart
* made the MPCexport MEX interface more consistent with the SIMexport MEX interface
* Merge branch 'master' of github.com:acado/acado
* added a simple example of a closed-loop simulation using MPCexport with SIMexport from MATLAB
* deleted IntermediateState as a keyword
* removed warning in DIRK integrators export
* fixed problem with model parameters
* - added linear output support for discrete time models and NARX models
* fixed bug related to time dependencies in time-continuous models
* - removed one warning in IRK export
* Fixed `#28 <https://github.com/LCAS/acado/issues/28>`_
* minor bug fix
* - DIRK methods can currently only be exported with forward sensitivity propagation
  - ERK methods can be exported without sensitivity propagation, just like IRK
* updated sim_export for simulation without sensitivity generation
* fixed bug related to continuous output for simulation without sensitivity generation
* adapted MATLAB MEX interface for exported IRK integrators to allow for simulation without sensitivity generation
* possible to export efficient IRK methods without sensitivity generation
* Merge branch 'master' of github.com:acado/acado
* improved the MEX interface for exported integrators
* support for different sensitivity generation techniques in exported integrators,
  currently only forward and no sensitivity propagation
* added -fPIC compiler flag for compilation of ACADO from MATLAB
* ignore some specific warnings thrown by clang when compiling ACADO from MATLAB
* restructuring of the code generation for integrators to allow multiple sensitivity generation techniques
  per integrator type
* fixed bug related to time dependencies in a nonlinear model
* Solved `#29 <https://github.com/LCAS/acado/issues/29>`_; Removed -gstabs+ for OSX
* fixed bug in MATLAB MEX interface related to fixed parameters
* - removed a deprecated feature that was unused in code generated integrators
  - added explicit support for time dependencies in nonlinear, continuous time models (for e.g. DMS)
* Changed the default message color to 0
* Merge branch 'master' of github.com:acado/acado
* Refactored the messages handling a bit
* Updated messages numbers in qpOASES embedded.
* fixed some bugs related to NARX models
* Merge branch 'master' of github.com:mvukov/acado
* Extended OCP and Objective classes to support extended functions.
  This is code generation related, only.
* Merge branch 'master' of github.com:acado/acado
* test
* bug fix for nonequidistant control grids
* added a comment stating the step size of the integrator, when fixed
* removed some remaining acadoPrintf calls
* Merge branch 'master' of github.com:acado/acado
* Added deep member copying for the ExportArgument class.
* added support for externally defined linear in- and output systems in the model
* Updated .gitignore
* Export of variables and arguments refactored.
  ... in order to reduce memory consumption of the code generator.
* Update CMake Find script
* added info to error message, related to index out of range, to strongly simplify debugging
* repaired a code generation example
* CMake build system is updated. Build shared libs only (by default).
  We are building now ACADO ONLY the shared lib (by default) on Unix like
  OSs, and static for MSVC. All other libs are built as static and linked
  against the main ACADO lib. That way, we only have to ship one library.
  Building of the static ACADO lib is optional, just set
  ACADO_BUILD_STATIC variable to ON.
  Building of the shared libs for Windows is disabled.
  qpOASES 3.0 build script is heavily modified, just to satisfy needs for
  building ACADO.
* split of the integrator type options in standard ACADO and code generation types, according to issue `#27 <https://github.com/LCAS/acado/issues/27>`_
* added minor feature: return the number of the output function when adding a new one
* added .obj files to be ignored by git version control
* Fixed one of the mem issues with ExportVariable.
* fix for Windows 64 bit C++ compilers
* Merge branch 'master' of git://github.com/ghorn/acado
* added support for externally defined nonlinear, discrete time models
* added support for general nonlinear, discrete time models
* another old bug fixed related to explicit RK methods and non equidistant control grids
* small fix related to NARX models
* fix for non equidistant control grids
* Merge pull request `#24 <https://github.com/LCAS/acado/issues/24>`_ from ghorn/master
  enable travis ci
* added travis ci file
* Temporarily fixed ExportVariableInternal bug related to indexing of a
  given ExportVariable
* Added option for arrival cost computations in MHE.
* Fixed bug in ExportIndex minus operator, enhanced export of for loops.
  When increment is "--" (-1 increment), the for-loop checks for: "final
  val" < "for-loop val".
* Fixed memory leak in export of fcn eval tree.
* Fixed a bug in exporting argument list.
  The bug occured when an argument was a real scalar.
* On OSX build only for 64-bit arch. by default
* Extended export of function calls.
  Not it is possible to call a function with defined integer argument.
* removed some warnings
* added support for NARX models
* Merge branch 'master' of git://github.com/mvukov/acado
* added empty gitignore files to keep certain directories in git
* Merge branch 'master' of git://github.com/rienq/acado
* Merge branch 'master' of github.com:mvukov/acado
* Merge branch 'master' of github.com:mvukov/acado
  Conflicts:
  cmake/acado.pc.in
* use "=" instead of ":" in pkg-config export
  Conflicts:
  cmake/acado.pc.in
* examples/.gitignore ignores all getting_started constructs
* Updated pkg-config script generation
* extended pkg-config for qpOASES embedded sources and header paths
* - added support for NARX models in modelContainer, modelData etc
  - start implementation of NARX export class
* CMake cleanup
* CMake examples scripts cleaned
* CMake stuff cleanup.
* Cleaning the CMake scripts...
* Updated git ignore and CMake main script
* Added experimental folder
* added the export of a NARX integrator
* files for a 'discrete time integrator'
* fixed 2 bugs, mentioned on the discussion forum
* Merge branch 'master' of github.com:acado/acado
* Examples git ignore updated...
* Create .gitignore
* Update .gitignore
* Create .gitignore
* removed constant pointers in case of external models (from CasADi)
* export of (ODE) functions with constant pointers
* const pointers
* Update README.md
* Create README.md
* small change in the MEX interface
* no export of compare or test files if not necessary
* small bug fix in integrate MEX function
* OpenMP extensions for implicit integrators debugged (hopefully)
* ExportFunction reverted
* - cleanup crane code generation example
* - bug fixes code generation on Windows (from MATLAB)
  - small bug fix related to external models
* Added generation of the pkg-config script
* added DIRK methods to the ACADO integrator suite
* - changed the interface to auto generated integrators (according to ticket `#10 <https://github.com/LCAS/acado/issues/10>`_ on SF)
  - cleanup of code for export of linear solvers
  - added DIRK methods (work in progress)
* small bug fix, reported on the Sourceforge discussion forum
* Small bug fix from Rien for non-equidistant grids.
* Small extension to Matrix class.
* added doxygen tutorial for ellipsoidal integrator
* OPENMP for auto generated implicit integrators
* Small bug with exporting of the for-loops.
* - refactoring in export integrators (mostly C++ code)
  - support of fixed parameters by MEX interface
  - updated getting_started example with fixed parameter
  - support of timings with MEX interface
  - small bug fixes MATLAB interface, related to codegen
* Memory footprint for the size of a working array of exported symbolic functions is reduced.
* Improved memory management in working array for code export of symbolic functions
* Inf constant bug fixed; Small improvements in codegen.
* fixed some VS compiler errors/warnings that occured in the interval class
* improved performance of string class, improved symbolic operators, fixed bugs in ellipsoidal integrator, improved performance of Taylor expansions of ODEs
* CG small update, added option for hard-coding the constraint values.
* Added -DLINUX to compiler options -- important for time measurements
* Bug fixes in CMake compiler options related to optimizations...
* clang related warning removed...
* Small update, related to code generation; Warning removed in the string class.
* Added CPU-time profiling functionality in ellipsoidal integrator
* fixed bugs in ellipsoidal integrator and powerint class, added tutorial examples for set valued integration
* Bug fix and performance improvement:
  - Taylor variable: private ctor moved to public to enable compilation with clang
  - Addition operator: isOneOrZero functionality is commented since it is performance bottleneck.
* fixed bugs in validated integrator, added examples
* added a validated integrator based on Taylor model propagation with ellipsoidal remainders
* Warning removed
* added set arithmetic functionality
* added symbolic generation of the Taylor coefficients of the solution of an ODE. The routine works for any expansion order (see examples/basic_data_structures/ode_taylor_expansion.cpp)
* added functionality to evulate symbolic ACADO functions at templated evaluation points. (for an example see /examples/basic_data_structures/templated_function_call.cpp)
* fixed error messages in ocp class
* VariablesGrid in matlab interface
* feature to set the names of the resulting MEX files after code generation
* solved bug in getDependencyPattern in expression.cpp
* bug fix in parameter estimation examples for Matlab interface
* small simplifications in the SIMexport examples
* bug fix in SIMexport, related to resetIntegrator
* Added a script for publishing API doc.
* fixed integrator mex template after previous commit
* Resetting of the integrators moved to the workspace struct.
* added examples on export of ACADO integrators in Matlab interface
* cleaned objects.m for the Matlab interface in trunk
* merge from branch to trunk (it compiles)
* Minor modifications to the Rien's branch
* export folders for examples
* renaming example folders
* merge from trunk to branch
* merge from trunk to branch
* renaming
* cleanup modifications to branch
* ModelContainer in Matlab interface
* modelData and modelContainer
* modelData and modelContainer
* Docygen tutorial is a bit more polished now
* update of the Matlab interface with recent modifications
* modifications to prepare for merge to trunk (header files)
* modifications to prepare for merge to trunk (source files)
* Updated Doxygen conf. script.
* CMake options updated; Some compiler warnings removed.
* CMake scripts updated. We install everything to /usr/local now. Bug http://sourceforge.net/p/acado/tickets/7/ closed.
* Polishing...
  - Added copy file function
  - Improved doc generation for ExportFunction
* merge fix from trunk to branch
* - complete merge from trunk to branch
  - partial merge from branch to trunk for the Matlab interface
* - complete merge from trunk to branch
  - partial merge from branch to trunk for the Matlab interface
* small improvements to Matlab interface on branch
* Code generation fancyfied a bit....
* Extended OCP class for LSQ linear terms -- related to code generation.
* ACADO Matlab interface: merge from branch to trunk
* ACADO Matlab interface: merge from branch to trunk
* solved a very rare bug in the Matlab interface, concerning constants in expressions
* small addition to the matlab interface
* minor bug fix
* merged trunk changes to branch
* refactoring C++ code IRK export: evaluation of matrix for linear system and computation of sensitivities for continuous output
* refactoring in export of IRK methods: sensitivity generation and computation of continuous output
* - minor refactoring of the export of linear solvers
  - resetIntegrator instead of rk_num
* A small bug in ExportTemplatedFile fixed.
* Codegen low level structures updated
* small modification to second example of previous commit
* two interesting examples added on how to use the SIMexport class with ODE/DAE models with continuous output, different options to set the integration as well as the measurement grid
* separate folders for code_generation examples
* clean up of examples folder
* added option to specify a more flexible integration grid, even with continuous output etc
* merged option from branch to trunk to export data as as "static constant"
* solved previous incomplete merge from branch into trunk.. :(
* merged Matlab interface from branch to trunk
* small fix in Matlab interface
* Implemented 3 options for specifying the measurement grid of increasing flexibility (and decreasing code efficiency), of which
  the most flexible option allows the user to change this grid of measurements fully online
* - removed some compiler warnings
* Codegen bug fixes for internal structures
* merge refactoring of irk_export.cpp from branch into trunk
* - export of IRK methods refactored based on recent changes in ExportIndex etc. resulting in
  more clear code (C++ as well as exported C code)
* -- Improved behaviour of the Power und PowerInt classes when exporting code (see Ticket 5)
  -- Added diag command to ACADO syntax (see Ticket 6)
  -- Added parameter support to auto-generated Simulink interface
  -- Safeguarded zero-dimensional array allocation when auto-generating qpOASES interface
  -- Fixed a number of warnings related to uninitialized variables at different places
* Rocket example reverted
* ExportIndex updated; supports modulo operation
* merge trunk to branch
* Minor bug fixes in codegen; Reusing indices works
* merge
* bug fix: constant data wrapped in ExportVariable no longer supported
* merge trunk to branch
* Export of condensing -- bug fixed...
* - Matlab interface bug (objects.m should also compile casadi symbolics)
* ExportIndex bug fix
* merge from trunk to branch + some refactoring for code integrators
* Code generation refactored; main point: introduced reference counted objects
* accidentally commited objects.m file
* trunk/src/code_generation/sim_export.cpp
  branches/branch-rien/include/acado/code_generation/integrators/irk_export.hpp
  branches/branch-rien/include/acado/utils/acado_types.hpp
  branches/branch-rien/src/code_generation/integrators/irk_export.cpp
  branches/branch-rien/src/code_generation/export_argument.cpp
  branches/branch-rien/src/code_generation/linear_solvers/gaussian_elimination_export.cpp
  branches/branch-rien/src/code_generation/linear_solvers/householder_qr_export.cpp
  branches/branch-rien/src/code_generation/export_module.cpp
  branches/branch-rien/src/symbolic_expression/expression.cpp
* trunk/src/code_generation/sim_export.cpp
  branches/branch-rien/include/acado/code_generation/integrators/irk_export.hpp
  branches/branch-rien/include/acado/utils/acado_types.hpp
  branches/branch-rien/src/code_generation/integrators/irk_export.cpp
  branches/branch-rien/src/code_generation/export_argument.cpp
  branches/branch-rien/src/code_generation/linear_solvers/gaussian_elimination_export.cpp
  branches/branch-rien/src/code_generation/linear_solvers/householder_qr_export.cpp
  branches/branch-rien/src/code_generation/export_module.cpp
  branches/branch-rien/src/symbolic_expression/expression.cpp
* mhe_export not publicly available yet
* new MEX support for MPC and MHE export + support for external C models
* Starting a new branch
* small update on expression handling in Matlab interface
* Inclusion of <memory> header fixed, for VC++ compiler
* previous commit was incomplete..
* code export is now fully supported by the MATLAB interface of ACADO
* Premature; rolled back to r65
* - external C models supported in code_generation
  - initial support for MPCexport in Matlab interface
* A not so quick fix for MATLAB build sys'
* quick fix templates problem in matlab interface
* final modification modeling matlab interface
* Bug fixes related to the GCC compiler; Cmake script for examples fixed
* updates to the Matlab interface for integrators
* OK, build system finaly works on Linux and OS X...
* Minor bug fix in the code generation
* Minor bug fix in the code generation
* Minor bug fix with the build system
* Build system cleanup; codegen closed loop example updated; Exported RTI scheme works again; csparse interface source put in a sigle file
* Clean-up of makefiles, Codegen upgraded, C99 type of export is not needed, we are ANSI C compliant again.
* deleted all Makefiles except for qpoases 3.0 makefiles
* Doxygen tutorial updated
* Doxygen tutorials finalized,
  CasADi parts included -- for reference counting which will be introduced in code-generation
* added the last examples with doxygen
* added a few examples
* Added a Make script for some backward compatibility with old Make based projects.
* ExportForLoop updated. start and final value, as well as increment are of type ExportIndex. This allows easy for-loop nesting.
* - working on improvements of the modeling power in the ACADO Matlab interface
* Even numbered examples added
* - minor fix in integrators: no export of unused loop variables
* - small updates in the user-friendliness of the Matlab interface
* Code generation related:
  - introduced a flag for OpenMP, work in progress
  - modified ERK integrators, for usage with OpenMP
  - updated Function (symbolic tools), name of the global export variable can be general (but still has to be revised and rewritten)
  - minor cleanup of unused code.
* - small addition to previous commit
* - implemented different formulation of IRK methods for DAE systems
  - more general output functions allowed
  - according update Matlab interface
* - added support for DAE systems in the matlab interface of the integrators
* - added support for continuous outputs in the matlab interface of the integrators
* initialization of sensitivities in case of explicit integrator is moved to the integrator code itself
* explicit integrators: the right-hand side is exported when needed
* Small update explicit integrators: the pure right-hand side gets exported now as well, which is useful for mex functions
* - bring syntax for Differential and Output equations closer to Matlab syntax
  - new template for evaluating the right-hand-side --> the standard Matlab integrators can be used as a reference
* support for output functions (deleted the old class)
* Matlab interface updated, resulting in a much more natural way to define the differential equation
* - copy example 2 and 4 from 'old' website
  - small updates in the Matlab interface (more following)
* - bug in auxiliary_functions: current_time declared twice
  - addTemplates to build in matlab
  - update of irk_export for indices in for loops
* Uuppss... A wrong line was commented in a file. Bug fixed.
* Code generation related:
  - ExportForLoop is NOT declaring index any more. Instead, ExportFunction is in charge of bookkeeping of indices used in for loops
  - Return value of a function is now properly defined.
  - NMPC and explicit integrator classes updated according to the new modifications.
* Fixed a bug in the templated file class.
* - update integrators: the model (right-hand side + derivatives) can now optionally be defined in a separate C file, provided by the user or software like casadi
* Code generation: nesting of for loops enabled
* - use simply export_templated_file (without subclass) if the template doesn't need a dictionary
* Minor CMake script update
* Code generation templates added
* Bug fixes in codegen module, related to prefix on data structures.
* Deleting the source files in the main codegen folder
* Deleting the header files in the main codegen folder
* Update header files depending on the moved header files
* The same rearrangements for the header files + update other header files that depend on this
* Small rearrangements for the integrators (separate subfolder within code generation)
* Start moving the integrator source files to subfolders
* In response to Ticket `#3 <https://github.com/LCAS/acado/issues/3>`_:
  - Export of data declaration for given variables is implemented. This holds for local variables only, i.e. the variables that are not in structures.
* Update CMakeList.txt
* Update CMakeList.txt
* Code generation module extension:
  - now it is possible to add a prefix on a structure (work in progress)
  - introduced new data types (work in progress)
  - minor cleanup
* Main doxygen script updated...
* - introduced M_PI define, for VS Cpp
  - added doxygen based tutorials -- initial commit
* CMake for Windows compiler options: unforced absolute Gnuplot path
* fixed some warnings related to multiple default constructors (in DoubleConstant and KalmanFilter) and type conversion (in UniformNoise and GaussianNoise)
* Main CMake script update:
  - Building of examples is enabled by default
* Minor cleaning -- related to compiler warnings
* Quick patch to enable usage of Gnuplot on Windows -- CMake related
* Main CMake script update
* Added a CMake script for compilation of code-generation examples
* Initial commit; ESAT SVN version: 3100
* Initial commit
* Contributors: Andres, Boris, Boris Houska, Greg Horn, Joachim Ferreau, Jonathan Jekir, Marc Hanheide, Milan Vukov, Rafael Saback, Rien Quirynen, Rory Yorke, Shahab Kaynama, ThomasBesselmann, Torstein Ingebrigtsen Bø, allura, ferreau, francesco-romano, mkotlyar, rienq
