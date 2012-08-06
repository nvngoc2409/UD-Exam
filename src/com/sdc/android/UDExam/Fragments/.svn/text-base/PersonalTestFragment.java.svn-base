package com.sdc.android.UDExam.Fragments;

import com.sdc.android.UDExam.Swipeytabs.R;
import com.sdc.android.UDExam.Swipeytabs.R.id;

import android.os.Bundle;
import android.support.v4.app.Fragment;
import android.view.ContextMenu;
import android.view.LayoutInflater;
import android.view.MenuItem;
import android.view.View;
import android.view.View.OnClickListener;
import android.view.ViewGroup;
import android.widget.Button;
import android.widget.LinearLayout;
import android.widget.TextView;

public class PersonalTestFragment extends Fragment implements OnClickListener{
	private Button bt_choise_subject_ps;
	private TextView subject_ps, suggest_ps, note_personal_test;
	private String[] SUBJECTS;
	private LinearLayout linear_subject, linear_suggest;
	@Override
    public View onCreateView(LayoutInflater inflater, ViewGroup container, Bundle savedInstanceState) {
        ViewGroup root = (ViewGroup) inflater.inflate(R.layout.personal_test, null);
        SUBJECTS = getResources().getStringArray(R.array.subjects);
        bt_choise_subject_ps = (Button) root.findViewById(id.bt_choise_subject_ps);
        bt_choise_subject_ps.setOnClickListener(this);
        subject_ps = (TextView) root.findViewById(id.subject_ps);
        subject_ps.setOnClickListener(this);
        suggest_ps = (TextView) root.findViewById(id.suggest_ps);
        linear_subject = (LinearLayout) root.findViewById(id.onChoiseSubject_ps);
        linear_subject.setOnClickListener(this);
        linear_suggest = (LinearLayout) root.findViewById(id.onChoiseSuggest_ps);
        linear_suggest.setOnClickListener(this);
        note_personal_test = (TextView) root.findViewById(id.note_personal_test);
        note_personal_test.setOnClickListener(this);
        note_personal_test.setSelected(true);
        this.registerForContextMenu(bt_choise_subject_ps);
        return root;
	}
	@Override
	public void onClick(View v) {
		if(v.getId() == id.bt_choise_subject_ps || v.getId() == id.onChoiseSubject_ps){
			bt_choise_subject_ps.showContextMenu();
		}
		
		if(v.getId() == id.onChoiseSuggest_ps){
			if(suggest_ps.getText().toString().trim().equals(getResources().getString(R.string.yes))) 
				suggest_ps.setText(R.string.no);
			else
				suggest_ps.setText(R.string.yes);
		}
		
		if(v.getId() == id.note_personal_test){
			note_personal_test.setSelected(false);
			note_personal_test.setSelected(true);
		}
	}
	
	@Override
	public void onCreateContextMenu(ContextMenu menu, View v, ContextMenu.ContextMenuInfo menuInfo) {
		createMenu(menu);
	}

	private void createMenu(ContextMenu menu) {
		for(String sub : SUBJECTS){
			menu.add(sub);
		}
	}
	
	@Override
	public boolean onContextItemSelected(MenuItem item) {
		return(applyMenuChoice(item) ||
  		super.onContextItemSelected(item));
  }

	private boolean applyMenuChoice(MenuItem item) {
		subject_ps.setText(item.getTitle());
		return true;
	}
}
