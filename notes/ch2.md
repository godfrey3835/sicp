### 2.2.2 Hierarchical Structures (階層式結構)

```scheme
;算leaves數量
(define (count-leaves x)
  (cond ((null? x) 0)
        ((not (pair? x)) 1)
        (else (+ (count-leaves (car x))
                 (count-leaves (cdr x))))))
```

### 2.2.3 Sequences as Conventional Interfaces

```scheme
; 算leaves的平方和, 如果leaves的值是奇數的話
(define (sum-odd-squares tree)
  (cond ((null? tree) 0)
        ((not (pair? tree))
         (if (odd? tree) (square tree) 0))
        (else (+ (sum-odd-squares 
                  (car tree))
                 (sum-odd-squares 
                  (cdr tree))))))
```
