# matplotlib
Demonstrations with matplotlib library

Added (Python with matplotlib and other libraries in) Jupyter notebooks I made during the course:
&nbsp;

&nbsp;&nbsp;&nbsp;   PH526x: Using Python for Research

&nbsp;&nbsp;&nbsp;   HarvardX
&nbsp;

&nbsp;

Valid Certificate ID
&nbsp;
ef0cfcd693e74fa2a60f169453395a4c

![Searle_matplotlib](https://github.com/programweb/matplotlib/assets/12736699/f7cea54b-6a29-41d4-bc45-44075a52f1a3)

```python
X, Y = np.meshgrid(X, Y)
R = np.sqrt(X**2 + Y**2)
Z = np.cos(R)
fig = plt.figure()
ax = fig.add_subplot(projection='3d')
ax.plot_surface(X, Y, Z, vmin=Z.min() * 1.7, cmap=cm.Oranges)
plt.rcParams["figure.figsize"] = (30,30)

Gx, Gy = np.gradient(Z)
G = (Gx**2+Gy**2)**.5
N = G/G.max()
surf = ax.plot_surface(
    X, Y, Z, rstride=1, cstride=1,
    facecolors=cm.jet(N),
    linewidth=0, antialiased=False, shade=False)
    
plt.show()
```
