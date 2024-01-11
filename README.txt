1. Cargar pdg y hacer git clone
2. Añadir campo <li><a href="{{ url_for('ver_pdf') }}">Manual</a></li>
3. from flask import Flask, render_template, send_from_directory
4. @app.route('/ver_pdf')
   def ver_pdf():
      pdf_path = os.path.join('static', 'Documentos', 'bbdd.pdf')
      return send_from_directory('static', pdf_path, as_attachment=False)
