+++
title = "Algebra"
author = ["root"]
draft = false
+++

Notes from readings of Aluffi's Algebra: Chapter 0.


## Monoids {#monoids}

A **monoid** is a triple (M,p,1), in which M is a non-vacuous set, p is an associative binary composition in M, and 1 is an element of M such that p(1,a) = a = p(a,1) for all \\(a \in M\\).

A monoid without an associative p is sometimes called a **monad**. If there is no requirement on 1, then its a **semigroup** (M,p).

A **submonoid** of a set M, contains 1 and N is closed under the product in M.

A submonoid of the monoid M(S) of all transformations of the set S is a **monoid of transformations** of S.


### Cayley's theorem {#cayley-s-theorem}

1.  Any monoid is isomorphic to a monoid of transformations.
2.  Any group is isomorphic to a transformation group.


## Groups {#groups}

A group is an ordered pair (G,\*), where G is a set (closed under \*) and \* is a binary operation satisfying the following axioms.

1.  \* is associative
2.  There exists an identity element
3.  For each a in G, there is an (double-sided) inverse element

If the operation is commutative within the group, then the group is abelian.

The order of an element x is the smallest positive integer n such that \\(x^n = 1\\).

A group is also a monoid all of whose elements has an inverse element.


### Dihedral groups {#dihedral-groups}

D_2n is the set of symmetries of a regular n-gon via moving it in rigid motion. |D_2n| = 2n.

The elements are r^i and s, where s is a reflection and r is a rotation

Properties:

1.  1, r, \\(r^2\\) ..., \\(r^{n-1}\\) are all distinct and \\(r^n\\) = 1, so \\(|r| = n\\).
2.  |s| = 2
3.  s != r^i for any i
4.  \\(sr^i \neq sr^j\\) for all i!=j, 0 &lt;= i,j &lt;= n-1.
5.  rs = sr^-1
6.  \\(r^i s = s r^{-i}\\)


### Generators and relations {#generators-and-relations}

Groups can be described with generators which is a subset of G such that every element of G can be written as a finite product of elements of S. G = &lt;S&gt;.

D_2n = &lt;r,s&gt;

Relations are any equations satisfied by the generators. Groups can be represented by a presentation of G.

D_2n = &lt; \\(r,s | r^n = s^2 = 1, rs = sr^{-1}\\)&gt;


### Symmetric groups {#symmetric-groups}

Let \\(\Omega\\) be any nonempty set and \\(S\_\Omega\\) to be the set of all bijections from \\(\Omega\\) to itself. Then \\(S\_\Omega\\) is a group under function composition.

Elements of a symmetric group S can be written in terms of its cycle decomposition.

A **group of transformations** is a subgroup of the symmetric group of S.

The order is the lcm of the size of the group's disjoint cycles.


### Fields {#fields}

A Field is a set F together with two binary operations \\(+\\) and \\(\cdot\\) on F such that \\((F,+)\\) is an abelian group and \\((F - \\{0\\},\cdot)\\) is also an abelian group, and the distributive law holds.

\\[
F^\times = F - \\{0\\}
\\]

\\[
GL\_n(F) = \\{ A \vert \text{A is an $n \times n$ matrix with entries from F and det(A) $\neq$ 0} \\}
\\]

is called the general linear group of degree n.

\\[
\mathbb{Z}/p\mathbb{Z} = \mathbb{F}\_p
\\]

which is a finite field.


#### Properties {#properties}

1.  if F is a field and \\(|F| < \infty\\), then \\(| F | = p^m\\) for some prime p and integer m.
2.  if \\(|F| = q < \infty\\), then \\(|GL\_n(F)| = (q^n-1)(q^n-q)(q^n-q^2)\ldots(q^n-q^{n-1})\\)


### Quaternion group {#quaternion-group}

\\[
Q\_8 = \\{1,-1,i,-i,j,-j,k,-k\\}
\\]


### Homomorphisms and Isomorphisms {#homomorphisms-and-isomorphisms}

Let \\((G,\star)\\) and \\((H,\diamond)\\) be groups. A map \\(\psi : G \mapsto H\\) such that

\\[
\psi(x \star y) = \psi(x) \diamond \psi(y) \text{  for all $x,y \in G$}
\\]

is called a homomorphism.

The map \\(\psi : G \mapsto H\\) is called an isomorphism and G and H are said to be isomorphic or of the same isomorphism type, written \\(G \cong H\\), if

1.  \\(\psi\\) is a homeomorphism and
2.  \\(\psi\\) is a bijection

If \\(\psi : G \mapsto H\\), then

1.  |G| = |H|
2.  G is abelian iff H is abelian
3.  for all \\(x \in G\\), \\(|x| = |\psi(x)|\\)

Any two cyclic groups of the same order are isomorphic


### Group properties {#group-properties}

1.  Any subgroup of a cyclic group is cyclic. If &lt;a&gt; is infinite, the subgroups not equal to 1 are infinite and \\(s \to \langle a^s\rangle\\) is a bijective map of \\(\mathbb{N}\\) with the set of subgroups of \\(\langle a \rangle\\). If \\(\langle a \rangle\\) is finite of order \\(r\\), then the order of every subgroup is a divisor of r and for every positive divisor q of r, there is exactly one subgroup of order q.
2.  Let g and h be elements of an abelian group G having finite relatively prime orders m and n respectively. Then o(gh) = mn.
3.  Let g be an element of a finite abelian group of maximal order. Then \\(\exp G = o(g)\\)
4.  Let \\(\exp G\\) be the smallest integer \\(e\\) such that \\(x^e = 1\\) for all \\(x \in G\\). A finite abelian group is cyclic iff \\(\exp G = |G|\\).


### Group actions {#group-actions}

A group action of a group G acting on a set A is a map from \\(G \times A\\) to A (written \\(g \cdot a\\) for all \\(g \in G\\) and \\(a \in A\\)) satisfying the following properties:

1.  \\(g\_1 \cdot (g\_2 \cdot a) = (g\_1g\_2)\cdot a\\), for all g1,g2 in G, a in A
2.  \\(1 \cdot a  = a\\), for all a in A.


### Orbits &amp; cosets {#orbits-and-cosets}

Let G be a group of transformations of a set S. Then G defines an equivalence relation on S of \\(x \sim\_G y\\) if \\(y = \alpha(x)\\) for some \\(\alpha \in G\\). The G-orbit of \\(x \in S\\) is the set \\(Gx = \\{\alpha(x) \vert \alpha \in G\\}\\). When there is just one orbit, that is, \\(S = Gx\\) for some x, G is a **transitive** group of transformations of the set S. e.g. \\(S\_n\\) is transitive on \\(\\{1,2,\ldots,n\\}\\).


### Congruences {#congruences}

A congruence is an equivalence relation which can be multiplied.


### Subgroups {#subgroups}


#### Some subgroups {#some-subgroups}

Let A be any nonempty subset of G.

<!--list-separator-->

-  Centralizers

    \\(g a g^{-1}\\) is called the conjugate of a by g.

    \\[
    C\_G(A) = \\{ g \in G \vert gag^{-1}=a \forall a\in A\\}
    \\]

<!--list-separator-->

-  Center

    \\[
    Z(G) = \\{ g \in G \vert gx = xg \forall x \in G\\}
    \\]

<!--list-separator-->

-  Normalizer

    Define \\(gAg^{-1} = \\{ gag^{-1} \vert a \in A\\}\\) as the conjugate of A by g.

    \\[
    N\_G(A) = \\{g \in G \vert gAg^{-1} = A\\}
    \\]

    Each g in the normalizer normalizes A.

    A subgroup of a group G is called normal if every element of G normalizes the group.

<!--list-separator-->

-  Stabilizer

    \\[
    stab\_G(s) = \\{g \in G | g \cdot s = s\\}
    \\]

<!--list-separator-->

-  Kernel

    Kernel of action of G on S

    \\[
    \ker = \\{ g\in G | g\cdot s = s \forall s \in S\\}
    \\]

<!--list-separator-->

-  Cosets

    For \\(N \leq G\\) and \\(g \in G\\)

    \\[
    gN = \\{gn | n \in N\\}
    \\]

    is a left coset. A right coset is defined similarly. Any element of a coset is a representative for the coset.


### Quotient groups {#quotient-groups}

Let \\(\phi : G\to H\\) be a homomorphism with kernel K. The **quotient group** or **factor group**, \\(G/K\\) is the group whose elements are the fibers of \\(\phi\\).


#### Cosets {#cosets}

Fibers of a homomorphism are the left cosets of the kernel. (Also the right).

**Theorem**

Let N be any subgroup of the gorup G. The set of left cosets of N in G form a partition of G. Furthermore, for all \\(u,v \in G\\), \\(uN = vN\\) iff \\(v^{-1}u \in N\\). In particular, \\(uN = vN\\) iff u,v are representatives of the same coset.

**Theorem**

Let G be a group and N be a subgroup of G.

The operation on the set of left cosets of N in G described by \\(uN \cdot vN = (uv) N\\) is well defined (the group action can be any arbitrary representative) iff \\(gng^{-1} \in N\\) for all \\(g \in G, n\in N\\)

If the above operation is well defined, it makes the set of left cosets of N into a group.

**Theorem**

Let N be a subgroup of group G.

TFAE

1.  N is a normal subgroup of G (note this is not transitive)
2.  \\(N\_G(N) = G\\)
3.  \\(gN = Ng \forall g\in G\\)
4.  The left cosets are made into a group
5.  \\(gNg^{-1} \subseteq N \forall g \in G\\)
6.  N is the kernel of some homomorphism

**Theorem**

If H and K are subgroups of a group, HK is a subgroup iff HK = KH.

If H and K are subgroups and \\(H \leq N\_G(K)\\), then HK is a subgroup of G.

<!--list-separator-->

-  Lagrange's theorem

    If G is a finite group, \\(H \leq G\\), then \\(|H|\\) divides \\(|G|\\).

    <!--list-separator-->

    -  Converses

        The converse, the group has a subgroup of order \\(n\\) for each divisor of |G| is true for finite abelian groups.

        **Theorem (Cauchy)**

        If G is a finite group and p is a prime dividing |G|, then G has an element of order p.

        **Theorem (Sylow's 1st theorem)**

        If G is a finite group of order \\(p^\alpha m\\), where p is prime and p does not divide m, then G has a subgroup of order \\(p^\alpha\\)

    <!--list-separator-->

    -  Corollaries

        1.  If G is a finite group and \\(x\in G\\), then the order of x divides the order of G.
        2.  If G is a group of finite order, then G is cyclic.
        3.  \\(|HK| = \frac{|H||K|}{|H\cap K|}\\)


#### Isomorphism theorems {#isomorphism-theorems}

These follow from the canonical decomposition of group homomorphisms into a projection, isomorphism and inclusion map.

1.  If \\(\phi : G\to H\\) is a homomorphism of groups, then \\(\ker \phi \unlhd G\\) and \\(G / \ker \phi \cong \phi(G)\\).

mote.php/dav/files/delargement

-   A homomorphism is injective iff its kernel is 1.

-   \\(|G : \ker \phi| = |\phi(G)|\\) This is equivalently the rank-nullity theorem.

<!--listend-->

1.  Let G be a group, and A,B be subgroups such that \\(A \leq N\_G(B)\\). Then AB is a subgroup of G, \\(B \unlhd AB\\), \\(A \cap B \unlhd A\\) and \\(AB/B \cong A/A\cap B\\).

2.  Let G be a group and let H and K be normal subgroups of G with \\(H \leq K\\). Then \\(K/H \unlhd G/H\\) and \\((G/H)/(K/H) \cong G/K\\)

3.  Let G be a group and N be a normal subgroup of G. Then there is a bijection from the set of subgroups A of G which contain N onto the set of subgroups \\(\bar{A} = A/N\\) of \\(G/N\\). In particular, every subgroup of \\(\bar{G}\\) is of the form A/N for some subgroup A of G containing N (namely, its preimage in G under the natural projection homomorphism form G to G/N). This bijection has the following properties.

    For all A,B subgroups of G, with N a subgroup of A and B,

    -   \\(A \leq B\\) iff \\(\bar{A} \leq \bar{B}\\)

    -   if \\(A \leq B\\), then \\(|B : A| = | \bar{B} : \bar{A}|\\)

    -   \\(\overline{\langle A,B \rangle} =  \langle \bar{A},\bar{B} \rangle}\\)

    -   \\(\overline{A\cap B} = \bar{A} \cap \bar{B}\\)

    -   \\(A \unlhd G\\) iff \\(\bar{A} \unlhd \bar{G}\\)


### Group actions {#group-actions}

An action is faithful if its kernel is the identity.

**Theorem**

Let G be a group, H a subgroup of G and let G act by left multiplication on the set A of left cosets of H in G. Let \\(\pi\_H\\) be the associated permutation representation afforded by this action.

1.  G acts transitively on A
2.  The stabilizer in G of the point 1H is the subgroup H
3.  The kernel of the action is \\(\ker \pi\_H = \cap\_{x\in G}xHx^{-1}\\) and \\(\ker \pi\_H\\) is the largest normal subgroup of G contained in H.

**Corollary (Cayley's Theorem)**

Every group is isomorphic to a subgroup of some symmetric group. IF G is a group of order n, then G is isomorphic to a subgropu of \\(S\_n\\).

**Corollary**

If G is a finite group of order n and p is the smallest prime dividing \\(|G|\\), then any subgroup of index p is normal.


#### Conjugation action {#conjugation-action}

Based on the earlier discussion on Lagrange's theorem,

**Theorem**

\\[
\vert S | = | Z | + \sum\_{a\in A}[G: G\_a]
\\]

where \\(G\_a\\) is the stabilizer and Z is the set of fixed points of the action.

**Corollary**

For a p-group acting on a finite set S, and letting Z be the fixed point set of the action,

\\[
\vert Z | \equiv |S | \mod p
\\]

We will now define Z to be the centralizer.

**Lemma**

Let G be a finite group. If G/Z(G) is cyclic, then G is commutative and G/Z(G) is trivial.

We may now derive the Class Formula

**Theorem (Class Formula)**

\\[
\vert G | = |Z(G)| + \sum\_{a\in A}[G:Z(a)]
\\]

**Corollary**

A non-trivial p-group has nontrivial center.

In fact, every group of order p^2 is commutative.


### Sylow's theorems {#sylow-s-theorems}

**Definition**

A p-Sylow subgroup of a finite group is a subgroup of order p^r where the order of G is p^r m and gcd(p,m) = 1.

**Theorem (Sylow's 1st theorem)**

If G is a finite group of order \\(p^\alpha m\\), where p is prime and p does not divide m, then G has a subgroup of order \\(p^\alpha\\)

Equivalently, if p^k divides the order of G, then G has a subgroup of order p^k.

**Theorem (Sylow's 2nd theorem)**

Let G be a ﬁnite group, let P be a p-Sylow subgroup, and let \\(H \subset G\\) be a p-group. Then H is contained in a conjugate of P: There exists g ∈ G such that \\(H \subset gPg^{-1}\\).

**Theorem (Sylow's 3rd theorem)**

Let p be a prime integer, and G be a finite group of order p^r m. If p does not divide m, then the number of p-sylow subgroups of G divides m and is congruent to 1 mod p.


## Rings {#rings}

A ring is an abelian group with a second binary operation which has the properties of a monoid, with distributive properties with +.


### Element properties {#element-properties}

\\(a\\) is a:

**Left-zero divisor**, if there is a \\(b\in R,b\neq 0\\) such that ab=0. \\(a\\) is non-zero-divisor iff left multiplication is an injective function.

**Left unit**, if there is a b such that ab=1. (invertible)
Properties:

-   Left multiplication is a surjective function (equivalent definition)
-   Right multiplication is injective / \\(a\\) is not a right zero-divisor
-   The inverse of a two-sided unit is unique
-   Two-sided unit form a group under multiplication.


### Types of rings {#types-of-rings}

**Integral domain**: A nonzero commutative ring such that ab=0 implies a=0 or b=0 (has no left-zero divisors). Thus cancellation laws work.

**Field**: A nonzero commutative ring where every nonzero element is a unit. (i.e. a nonzero commutative division ring) All fields are integral domains. All integral domains are fields when the ring is finite. It can be shown using **Wedderburn's little theorem** that finite division rings necessarily commute.

A field is algebraically closed if for every non-constant f(x) in k[x] there is a r such that f(r) = 0. e.g. the complex field.

The only ideals of a field is the trivial ideal and itself.

**Subring**: A ring whose subset inclusion function is a ring homomorphism.

**Noetherian**: A commutative ring whose every ideal is finitely generated.

**Principal Ideal domain (PID):** An integral domain where whose every ideal is principal.

**Unique Factorization domain (UFD):**


### Polynomial rings {#polynomial-rings}

A polynomial is a finite linear combination of monomials in a certain indeterminate with ring elements as coefficients. Polynomial rings clearly inherit properties such as commutativity, Noetherian, integral domain and UFD. Those inherited from fields are PIDs.


### Cayley's theorem analog for rings {#cayley-s-theorem-analog-for-rings}

The function \\(r\mapsto \lambda\_r, \lambda : R \to End\_{Ab}( R)\\) is an injective ring homomorphism.


### Ideals {#ideals}

A subgroup I of R is a left ideal if \\(rI \subset I\\) for all \\(r \in R\\). In general, the only ideal containing 1 is the ring itself.

Ideals define a canonical projection, in fact a projection from R-&gt;R/I is a ring homomorphism iff I is an ideal of R. Every ideal is the kernel of some ring homomorphism and all kernels are ideals. The canonical decomposition lead to analogs of the isomorphism theorems for rings.

Ideals may be generated by multiplication of a ring element with the ring. In the commutative case, aR is denoted by (a). Intersections and products of ideals are ideals. Products of ideals are subsets of their intersection. The sum of ideals is also an ideal. Each element of this ideal is a linear combination of the elements generating the ideals. These ideals are finitely generated. These lead to the defintions of Noetherian and PIDs (defined above). While Z is a PID, Z[x] isn't.

**Theorem**

Let R be a commutative ring, and f(x) a monic polynomial of degree d. The function \\(\varjphi: R[x] \to R^{\otimes d}\\) defined by sending \\(g(x) \in R[x]\\) to the remainder of the division of g by f induces an isomorphism of abelian groups, \\(R[x]/(f(x)) \cong R^{\otimes d}\\).


### Primes and maximal ideals {#primes-and-maximal-ideals}

**Definition**

Let I be a proper ideal of a commutative ring.

-   I is a **prime ideal** if \\(R/I\\) is an integral domain.
-   I is a **maximal ideal** if \\(R/I\\) is a field. (maximal implies prime)

Equivalently,

-   I is prime iff for all \\(a,b \in R\\)

\\[
 a b \in I \implies (a\in I \text{ or } b \in I)
\\]

The equivalence is related to the nature of cancellation on integral domains.

-   I is maximal iff for all ideals of R,

\\[
 I \subseteq J \implies (I = J \text{ or } J = R)
\\]

This follows from a commutative ring being a field iff its ideals are (0) and (1).

**Properties:**

-   By Zorn's lemma (this is not required in Noetherian rings), every nonzero ring has a maximal ideal.
-   A ring with exactly one maximal ideal m is a **local ring** (such as fields). The field A/m is called the **residue field** of A. If A is a ring and there is a proper ideal such that every \\(x \in A - m\\) is a unit in A, then A is a local ring and m its maxmimal ideal. If every element of 1+m  is a unit in A, then A is a local ring.
-   A ring with finitely many maximal ideals is called **semi-local.**

Prime and maximal are equivalent under these cases:

-   I is an ideal of a commutative ring and R/I is finite. This follows from the earlier proposition on equivalence between fields and integral domains for finite rings.
-   R is a PID and I is a nonzero ideal in R.


#### Polynomial rings {#polynomial-rings}

The set of prime ideals of a commutative ring is called the **spectrum** of R.

The krull dimension of a commutative ring is the length of the longest chain (by inclusion) of **prime** ideals in R. PIDs and fields necessarily have dimension 1 (Why?). Using Hilbert's Nullenstatz however, it can be shown that the Krull dimension of k[x1,x2,...,xn] is precisely n.

For polynomials induced by an algebraically closed field, the maximal ideals are exactly those of the form (x-c).


### Modules {#modules}

R-modules are abelian groups endowed with an action of R. The left action fulfills the following requirements.

1.  The two kinds of distributivity
2.  \\(rs \cdot m\\) = \\(r\cdot (s\cdot m)\\)
3.  Existence of identity action.

Note the similarity with scalar multiplication in vector spaces.

Every abelian group is a Z-module in exactly one way, as Z is initial in the category of Ring.

**Definition**

In a commutative ring, an R-algebra is a ring homomorphism \\(\alpha: R\to S\\) such that \\(\alpha( R)\\) is contained in the center of S. this allows \\((r\_1s\_1)(r\_2s\_2) = (r\_1r\_2)(s\_1s\_2)\\).


#### Submodules &amp; Quotients {#submodules-and-quotients}

A submodule N is a subgroup preserved by the action of R. That is rn is in N for all r and n. This is akin to ideals and thus submodules are exactly the ideals of R.

rM where r is in the center of R and M is an R-module is a submodule of M. If I is any (left)-ideal, \\(IM = \left\\{\sum\_i r\_i m\_i \vert r\_i \in I, m\_i \in M\right\\}\\) is a submodule. A submodule has a corresponding canonical projection, and thus for all submodules N, the corresponding quotient group is an R-module on M/N.

If R is a ring and I is a two-sided ideal of R, then I, R and R/I are R-modules. I is a submodule of R, and R and R/I are R-algebras if R is commutative.

The three ismomorphism theorems also follow.


#### Noetherian modules {#noetherian-modules}

A module is finitely generated

**Theorem**

On an R-module V, every submodule of V is finitely generated iff it fulfills the ascending chain condition (a.c.c): There is no infinite strictly increasing chain of submodules of V.

An R-module M is noetherian if every submodule of M is finitely generated as an R-module. Equivalently, a ring is notheritan iff it is noetherian as a module over itself.

**Theorem**

Let M be an R-module, and N a submodule of M. then M is Noetherian iff both N and M/N are Noetherian.


#### Generation of R-algebras {#generation-of-r-algebras}

An R-algebra is **finitely generated** as a module over R if there is an onto homomorphism of R-modules from the free R-module on a finite set to S. (Think vector spaces). S is thus **finite type**.

An R-algebra is **finitely generated** as an algebra if there is an onto homomorphism of R-algebras from the free R-algebra on a finite set to S. (Think complex numbers or polynomial rings). S is thus called of **finite type.**

Finite implies finite type but not the other way around, like the polynomial ring.


## Irreducibility and factorization {#irreducibility-and-factorization}

{{< figure src="./aluffione.png" >}}

By default, we will be only considering commutative rings which are integral domains.

Recall that a ring is Noetherian if every ideal of R is finitely generated.

**Proposition**

R is a commutative ring and M is an R-module.

TFAE:

-   M is noetherian.
-   M fulfills the acc condition
-   Every nonempty family of submodules of M has a maximal element w.r.t. inclusion

**Theorem**

Let R be a Noetherian ring, and J be an ideal of the polynomial ring \\(R[x\_1,\ldots,x\_n]\\). Then the ring \\(R[x\_1,\ldots,x\_n]/J\\) is Noetherian.

This follows from the Hilbert's basis theorem, and expresses the fact that every finite-type algebra over a Noetherian ring is Noetherian.

**Lemma (Hilbert's basis theorem)**

\\(R\\) noetherian implies \\(R[x\_1,\ldots,x\_n]\\) Noetherian.


### Prime and irreducible elements {#prime-and-irreducible-elements}

**Definition**

\\(a,b\in R\\) where R is a (commutative) ring. \\(a \vert b\\) if \\(b \in (a)\\). Two elements are associates if \\((a) = (b)\\), or when a|b and b|a.

In integral domains, we can relax the definition of associates to:

**Lemma**

Let a,b be nonzero elements of an integral domain R. Then a and b are associates iff \\(a = ub\\) for some unit u in R.

**Definition**

Let R be an integral domain.

An element \\(a\\) is **prime** if the ideal \\((a)\\) is prime; that is, a is not a unit and:

\\[
a | bc \implies (a | b \text{ or } a | c)
\\]

An element \\(a\\) is **irreducible** if a is not invertible (not a unit) and

\\[
a=bc \implies (\text{b is a unit or c is a unit})
\\]

Some other definitions include:

**Definition**

A nonunit \\(a\\) is irreducible iff

-   a = bc implies that a is an associate of b or of c
-   a = bc implies (a) = (b) or (a) = (c)
-   \\((a) \subseteq (b) \implies (b) = (a)\\)  or \\((b) = (1)\\).
-   (a) is maximal among proper principal ideals (rephrasing the previous point)

It can be shown that in an integral domain, a non zero prime element is always irreducible. The converse holds in UFDs.


### Factorization {#factorization}

An element in an integral domain has a factorization into irreducibles if it is equal to a product of irreducible elements. The factorization is unique if the elements are determined up to order and associates.

**Definition**

An integral domain is a **domain with factorization** if every nonzero, non-invertible element has a factorization into irreducibles. If the factorizations are unique, the domain is called **factorial** or a **unique factorization domain (UFD)**.

Here are some conditions for factorizations to exist:

-   If every ascending chain of principal ideals starting with a nonzero, non-invertible element stabilizes, then that element has a factorization into irreducibles.
-   Noetherian rings fullfill the a.c.c so factorizations exist in them.


### UFDs {#ufds}

Alternate definitions:

-   The acc for principal ideals holds in R and every irreducible element of R is prime.

Properties:

Let R be a UFD, and a,b,c be nonzero elements of R.

-   \\((a) \subseteq (b)\\) \\(\iff\\) the multiset of irreducible factors of b is contained in the multiset of irreducible factors of a.
-   a and b are associates iff the two multisets coincide
-   the irreducible factors of a product 'bc' are the collection of all irreducible factors of b and of c.
-   All PIDs are UFDs.

In UFDs, the gcd always exists, where we define the gcd as an element d such that d | a and d | b and any element which also divides a and b also divides d. This can be shown by constructing the gcd from the 'prime factorization' as with integers.


### Euclidean domains {#euclidean-domains}

Rings where one can perform division with remain (recall euclid's algorithm).

**Definition**

A **valuation** on an integral domain is any function \\(v : R\ \\{0\\} \to \mathbb{Z}^{\geq 0}\\).
A **Euclidean valuation** on an integral domain is a valuation such that for all a and nonzero b, there exist q and r such that:

\\[
a = qb + r
\\]

with either \\(r=0\\) or \\(v( r) < v(b)\\). An integral domain is a **Euclidean domain** if it admits a Euclidean valuation.

Euclid's algorithm can thus be proved by noting that \\(a = bq + r \implies (a,b) = (b,r)\\). Thus \\(\gcd(a,b) = \gcd(b,r)\\). (given it exists)


### Unique factorization in polynomial rings {#unique-factorization-in-polynomial-rings}

We would like to establish that R[x] is a UFD when R is a UFD. But first we would need to prove Gauss' lemma and introduce the idea of primitivity.

**Definition**

Let R be a commutative ring and let \\(f(x) \in R[x]\\). \\(f\\) is **primitive** if for all principal prime ideals \\(\mathfrak{p}\\), \\(f \notin \mathfrak{p}R[x]\\). If the requirement of being principal is removed, then you could call it 'very primitive'.

Products of polynomials are primitive iff the constituents are primitive.

**Properties:**

-   f is very primitive iff \\((a\_0,\ldots,a\_d) = (1)\\).
-   If R is a UFD, then f is primitive iff \\(\gcd(a\_0,\ldots,a\_d)=1\\).

**Definition**

The **content** of a nonzero polynomial \\(f \in R[x]\\) denoted \\(cont\_f\\) is the gcd of its coefficients. Uniqueness is only definde up to units but usually only the principal ideal generated by the content matters.

**Properties:**

Let R be a UFD and \\(f \in R[x]\\). Then,

-   \\((f) = (cont\_f)(\underbar{f})\\), where \\(\underbar{f}\\) is primitive.
-   if \\((f) = ( c)(g)\\) with \\(c\in R\\) and \\(g\\) primitive, then \\(( c) =(cont\_f)\\).

We may now cite Gauss' lemma

**Theorem**

Let R be a UFD, and \\(f,g \in R[x]\\). Then,

\\[
(cont\_{fg})=(cont\_f)(conf\_g)
\\]

Thus when \\((f) \subseteq (g)\\), then \\((cont\_f)\subseteq (cont\_g)\\)


### Localization and the field of fractions {#localization-and-the-field-of-fractions}

The field of fractions is the smallest field containing R. K(Z) = Q.

**Definition**

The field of rational functions is the field of fractions of the ring R[x].

**Theorem**

If R is a UFD and K is the field of fractions of R, then a nonconstant polynomial in R is irreducible in R[x] iff it is irreducible in K[x] and primitive.

Using this construction, we can show that if R is a UFD, then R[x] is a UFD. (Analagous to Hilbert's basis theorem). Note that this does not apply to power series as counter examples exist.

The idea is that since K is a field thus K[x] is a PID hence a UFD, it can be prime factorized, and by the earlier theorem factorization of K[x] is essentially factorization in K[x].


### Irreducibility of polynomials {#irreducibility-of-polynomials}

Preliminary results:

-   The number of roots of a polynomial induced by an integral domain is at most n. This can be shown by noting that K(R)[x] can have at most n roots corresponding to its irreducible degree 1 factors.
-   If R is an infinite integral domain, then for f,g in R[x], f = g iff \\(r\mapsto f( r)\\), \\(r\mapsto g( r)\\) agree. This shown by noting a nonzero polynomial can't have infinite roots.
-   A polynomial of degree 2 or 3 in a polynomial ring induced by a field is irreducible iff it has no roots.


#### Algebraically closed fields {#algebraically-closed-fields}

We can construct algebraic extension to a field to add more roots. A homomorphism of fields is necessarily injective so the inclusion map is quite natural.

**Theorem**

Let k be a field, and \\(f(t) \in k[t]\\) be a nonzero irreducible polynomial. Then,

\\[
F :=k[t] / (f(t))
\\]

is a field endowed, with a natural homomorphism (\\(k \to k[x] \to F\\)), realizing it as an extension of k. Further, if \\(f(x) \in k[x] \subseteq F[x]\\) has a root in F, namely the coset of t.

It is a field because k is a field thus k[t] is a PID, all PIDs are UFDs and thus f(t) irreducible implies prime implies maximal thus the quotient is a field.

<!--list-separator-->

-  Algebraic closure

    **Definition**

    A field is **algebraically closed** if all irreducible polynomials in k[x] have degree 1 iff every nonconstant polynomial factors completely as a product of linear factors iff every nonconstant polynoimal has a root in k.

    Similar to Euclid's argument proving the infinitude of prime integers, algebraically closed fields are infinite.

<!--list-separator-->

-  Polynomials

    We may ask if irreduciblity is preserved to some extent under homomorphisms.

    For example for Z[x],

    **Proposition**

    let \\(f \in \mathbb{Z}[x]\\) be a primitive polynomial, and p a prime integer. If f mod p has the same degree as f and is irreducible in \\(Z/pZ[x]\\), then f is irreducible in Z[x].

    But in general there are irreducible polynomials which are reducible modulo all primes.

    **Theorem (Eisenstein's criterion)**

    Let R be a (commutative) ring, and let \\(\mathfrak{p}\\) be a prime ideal of R.

    If a polynomial fulfills,

    1.  \\(a\_n \notin \mathfrak{p}\\)
    2.  \\(a\_i \notin \mathfrak{p}\\) for \\(0 \leq i < n-1\\)
    3.  \\(a\_0 \notin \mathfrak{p}^2\\).

    Then f is not the product of polynomials of degree &lt; n in R[x].

    In particular it says that cyclotomic polynomials with prime number of terms are irreducible.


### Chinese remainder theorem {#chinese-remainder-theorem}

How much information is needed to reconstruct an integer based on its modulo classes?

Assume commutative ring.

**Theorem**

Let \\(I\_1,\ldots,I\_k\\) be ideals of R such that \\(I\_i + I\_j = (1)\\) for all \\(i\neq j\\). Then the natural homomorphism

\\[
\varphi : R \to \frac{R}{I\_1} \times \ldots \times \frac{R}{I\_k}
\\]

is surjective and induces an isomorphism

\\[
\tilde{\varphi} : \frac{R}{I\_1\ldots I\_k} \tilde{\to} \frac{R}{I\_1} \times \ldots \times \frac{R}{I\_k}
\\]

In PIDs since gcd(a,b) = 1 iff (a,b) = (1) as ideals,

**Corollary**

Let \\(a\_i \in R\\) be the elements such that \\(\gcd(a\_i,a\_j) = 1\\) for all \\(i\neq j\\). Let \\(a = a\_1\ldots a\_k\\). Then the map

\\[
\varphi : \frac{R}{(a)} \to \frac{R}{(a\_1)} \times \ldots \times \frac{R}{(a\_k)}
\\]

defined by \\(r + (a) \mapsto (r+(a\_1),\ldots,r+(a\_k))\\) is an isomorphism.


### Gaussian integers {#gaussian-integers}

Gaussian integers are an example of Euclidean domains besides the integer ring and F[x] where F is a field.

\\[
\mathbb{Z}[i] := \frac{Z[x]}{(x^2 + 1)}
\\]


## Linear algebra {#linear-algebra}


### Bases {#bases}

**Definition**

An indexed set is a basis if it generates an R-module and is linearly independent

While bases are necessarily maximal linearly independent subsets and minimal generated subsets, modules over a field allow the converse to hold.

In fact, over fields a subset B of a vector space is a basis iff it is a maxmial linearly independent subset iff it is a minimal generating set.


## Fields {#fields}

When studying fields we may focus on field extensions. In fact every field extends Z as Z is initial in Fld.

One invariant of fields is its characteristic.

**Definition**

The **characteristic** of a field k is the nonnegative generator of the kernel (an ideal) of the unique ring homomorphism from Z to k.


### Field extensions {#field-extensions}

**Definition**

A field extension \\(k \subseteq F\\) is finite, of degree n, if F has finite dimension n as a vector space over k. The extension is infinite otherwise. The degree of a finite extension is denoted by [F:k].

A particular type of field extensions are simple extensions

**Definition**

Let \\(k\subseteq F\\) is a field extension, and let \\(\alpha \in F\\). The smallest subfield of F containing both \\(k\\) and \\(\alpha\\) is denoted \\(k(\alpha)\\). A field extension is **simple** if there exists an element \\(\alpha \in F\\) such that \\(F =k(\alpha)\\).

**Theorem**

Let \\(k \subseteq k(\alpha)\\) be a simple extension. Consider the evaluation map, \\(\epsilon : k[t] \to k(\alpha)\\), defined by \\(f(t) \mapsto f(\alpha)\\).

-   \\(\epsilon\\) is injective iff \\(k \subseteq k(\alpha)\\) is an infinite extension. In this case, \\(k(\alpha)\\) is isomorphic to the field of rational functions \\(k(t)\\).
-   \\(\epsilon\\) is not injective iff \\(k \subseteq k(\alpha)\\) is finite. In this case there exists a unique monic irreducible nonconstant polynomial \\(p(t) \in k[t]\\) of degree \\(n = [k(\alpha) : k]\\) such that:

\\[
k(\alpha) \cong \frac{k[t]}{(p(t))}
\\]

Via this isomorphism, \\(\alpha\\) corresponds to the coset of \\(t\\). The polynomial \\(p(t)\\) is the monic polynomial of smallest degree in \\(k[t]\\) such that \\(p(\alpha) = 0\\) in \\(k(\alpha)\\).

**Definition**

The group of automorphisms of the extension denoted \\(Aut\_k(F)\\) is the group of field automorphisms \\(j : F \to F\\) such that \\(j|\_k = id\_k\\).

In particular, let \\(k\subseteq F = k(\alpha)\\) be a simple finite extension, and \\(p(x)\\) be the minimal polynomial of \\(\alpha\\) over \\(k\\). Then \\(|Aut\_k(F)|\\) equals the number of distinct roots of \\(p(x)\\) in F.

\\[
\vert Aut\_k(F) | \leq [F:k]
\\]

with equality iff \\(p(x)\\) factors over \\(F\\) as a product of distinct linear polynomials.


#### Algebraic extensions {#algebraic-extensions}

**Definition**

Let \\(k\subseteq F\\) be a field extension, and \\(\alpha \in F\\). Then \\(\alpha\\) is **algebraic** over k, of degree n, if \\(n = [k(\alpha):k]\\) is finite; it is transcendental over k otherwise.

An extension is algebraic if ever \\(\alpha \in F\\) over k.

By the earlier characterisation, an element is algebraic iff there exists a nonzero polynomial \\(f(x) \in k[x]\\) such that \\(f(\alpha)=0\\).

Finite extensions are necessarily algebraic.

**Definition**

A field extension is **finitely generated** if there exist \\(\alpha\_1,\ldots,\alpha\_n \in F\\) such that,

\\[
F = k(\alpha\_1)(\alpha\_2)\ldots(\alpha\_n)
\\].

**Properties:**

Let \\(k \subseteq F = k(\alpha\_1,\ldots,\alpha\_n)\\) be a finitely generated field extension. TFAE,

1.  \\(k\subseteq F\\) is a finite extension
2.  \\(k\subseteq F\\) is an algebraic extension
3.  Each \\(\alpha\_i\\) is algebraic over k.

If the conditions are satisfied, then the degree of the extension is less than or equal to the product of the individual degrees of \\(\alpha\_i\\) over k. In fact this shows that addition, products, and quotients of algebraic roots are also algebraic.

The set of algebraic elements of any extension also forms a field. Composition of algebraic extensions are algebraic.


### Algebraic closure {#algebraic-closure}

Recall a field is algebraically closed if all irreducible polynomials in F[x] have degree 1.

Every field admits an algebraic closure unique up to isomorphism.

**Theorem (Nullstellensatz)**

Let \\(k \subseteq F\\) be a field extension, and that F is a finite-type k-algebra. Then \\(k \subseteq F\\) is a finite (thus algebraic) extension.


### Other types of field extensions {#other-types-of-field-extensions}

**Definition**

Let k be a field, and f(x) in k a polynomial of degree d. The **splitting field** for f(x) over k is an extension F of k such that

\\[
f(x) = c\prod\_{i=1}^d (x-\alpha\_i)
\\]

splits in \\(F[x]\\), and further \\(F = k(\alpha\_1,\ldots,\alpha\_d)\\) is generated over k by the roots of f(x) in F.

**Theorem**

The splitting field F for f over k is unique up to isomorphism and \\([F:k] \leq (\deg f)!\\).

**Definition**

A field extension is **normal** if for every irreducible polynomial f(x) over k, f(x) has a root in F iff f(x) as a product of linear factors over F.

**Theorem**

A field extension is finite and normal iff F is the splitting field of some polynomial over k.


### (Some) Galois theory {#some--galois-theory}

**Definition**

Let \\(k\subset F\\) be a field extension, and \\(G \subseteq Aut\_k(F)\\) be a group of automorphisms of the extension. The fixed field is the intermediate field,

\\[
F^G := \\{ \alpha \in F | \forall g \in G, g\alpha = \alpha \\}
\\]