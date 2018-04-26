#### Articles
- [Markdown for Jupyter Notebooks Cheatsheet](https://medium.com/ibm-data-science-experience/markdown-for-jupyter-notebooks-cheatsheet-386c05aeebed)

#### Stack Overflow
- [How to show (as output cell) the contents of a .py file with syntax highlighting?](https://stackoverflow.com/questions/19197931/how-to-show-as-output-cell-the-contents-of-a-py-file-with-syntax-highlighting)

    ```python
    from pygments import highlight
    from pygments.lexers import PythonLexer
    from pygments.formatters import HtmlFormatter
    import IPython

    with open('my_file.py') as f:
        code = f.read()

    formatter = HtmlFormatter()
    IPython.display.HTML('<style type="text/css">{}</style>{}'.format(
        formatter.get_style_defs('.highlight'),
        highlight(code, PythonLexer(), formatter)))
    ```
