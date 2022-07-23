FROM jupyter/scipy-notebook

# jupyter password設定
# RUN jupyter notebook --generate-config
RUN echo "c.NotebookApp.password = 'sha1:099fb02aae7d:8350f59667778656fffd0859a028ee90a28ef5bc'" >> ~/.jupyter/jupyter_notebook_config.py

RUN pip install --upgrade pip && pip install \
    neo4j \
    openpyxl