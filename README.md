# NumAlScripts

BISECTION
function (p, msg) = binaryFunc(a,b,TOL, N0, f)
  i = 1;
  FA = f(a);
  
  while i < N0
    p = a + (b-a)/2;
    FP = f(p);
    if FP = 0 or (b-a)/2 = TOL
      fprintf p;
      end
    i = i + 1;
    if FA * FP > 0
      a = p;
      FA = FP;
    else
      b = p;
    endif
  endwhile
  fprintf 'method failed after N0 iterations, N0 =', N0;
  end
