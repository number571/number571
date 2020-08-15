    Learning as a kind of hobby.
```scheme
(define (cons x y)
    (define (dispatch m)
        (cond ((= m 0) x)
              ((= m 1) y)
              (else (error "m /= {0, 1}"))))
    dispatch)
(define (car f) (f 0))
(define (cdr f) (f 1))
```
